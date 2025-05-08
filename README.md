# FIAP - Faculdade de Informática e Administração Paulista 

<p align="center">
<a href= "https://www.fiap.com.br/"><img src="assets/logo-fiap.png" alt="FIAP - Faculdade de Informática e Admnistração Paulista" border="0" width=40% height=40%></a>
</p>

<br>

# Projeto Integrado - FPF Enterprises  
**Grupo:** FPF Enterprises  
**Integrantes:**  
- Pedro Henrique Zani - PEDROHZANI@GMAIL.COM  
- Flavia Nunes Bocchino - flahbocchino@gmail.com  
- Felipe Silva de Menezes - menezes.felipesilva@gmail.com  

---

# 🧠 Proposta Técnica – FPF Enterprises  
**Fase 1 – Planejamento e Estruturação Técnica**  
**Desafio:** Coleta, Armazenamento e Processamento Local de Dados Sensoriais para Predição de Falhas  

---

## 1. 🎯 Justificativa do Problema  
Em ambientes produtivos como o agronegócio e a indústria, falhas inesperadas em máquinas e sistemas geram atrasos, desperdícios e prejuízos. A ausência de um sistema inteligente que antecipe essas falhas com base em dados operacionais limita a eficiência e impede a adoção de estratégias preditivas.

A **FPF Enterprises** propõe o desenvolvimento de uma arquitetura tecnológica baseada na coleta de **dados sensoriais reais**, com **armazenamento em nuvem** e **processamento local** usando Machine Learning. O objetivo é antecipar falhas, permitindo a tomada de decisões corretivas com antecedência e confiabilidade.

---

## 2. 💡 Descrição da Solução Proposta  
A solução consiste em um sistema que:
- Coleta dados sensoriais (ex.: vibração, temperatura, umidade, velocidade) com sensores físicos (ESP32);
- Armazena esses dados em um **banco de dados PostgreSQL** hospedado em nuvem (AWS RDS);
- Processa localmente os dados no computador do operador usando Python;
- Treina modelos preditivos com TensorFlow para antecipar falhas de componentes ou sistemas operacionais.

### 🌟 Benefícios Esperados:
- **Redução de tempo de inatividade:** previsões precisas permitem manutenção antes que a falha aconteça;
- **Economia de recursos:** intervenções planejadas evitam desgaste desnecessário de componentes;
- **Aumento da confiabilidade operacional:** monitoramento constante e preditivo melhora a tomada de decisão.

---

## 3. 🛠️ Tecnologias Utilizadas

| Categoria                  | Ferramenta                     | Justificativa                                      |
|---------------------------|--------------------------------|-----------------------------------------------------|
| Linguagem de Programação   | Python                          | Sintaxe acessível, ideal para ciência de dados e IA  |
| Bibliotecas de IA          | TensorFlow, Keras, Scikit-learn  | Frameworks poderosos e amplamente usados em predição |
| Manipulação de Dados       | Pandas, NumPy                    | Manipulação rápida e eficiente de dados tabulares    |
| Banco de Dados             | PostgreSQL (AWS RDS)             | Armazenamento relacional seguro, com backup automático|
| Sensores                   | ESP32                           | Leitura de variáveis em tempo real com conexão Wi-Fi |
| Nuvem                      | Amazon Web Services (RDS)        | Alta disponibilidade, escalabilidade e integração    |
| IDE / Ambiente Local       | Jupyter Notebook                 | Análise interativa e visualização de dados           |

---

## 4. 📐 Esboço da Arquitetura da Solução

1. **Coleta de Dados:**  
   - Sensores ESP32 capturam variáveis críticas (temperatura, vibração).  
   - Cada leitura contém um **timestamp**, **ID do sensor** e **variáveis coletadas**.  
   - Dados enviados via Wi-Fi para o banco na nuvem.  

2. **Armazenamento na Nuvem:**  
   - Banco de dados PostgreSQL (AWS RDS) recebe e organiza os dados.  
   - Estrutura relacional garante rastreamento por data/hora e dispositivo.  

3. **Processamento Local:**  
   - Aplicação em Python conecta ao banco e coleta os dados.  
   - Modelos preditivos com TensorFlow identificam falhas potenciais.  

4. **Predição de Falhas:**  
   - Modelos classificam o estado dos equipamentos: **"Normal"** ou **"Risco de Falha"**.  

---

## 5. 🔎 Estratégia de Coleta de Dados  
- **Captura:** Sensores ESP32 coletam dados a cada 5 segundos.  
- **Envio:** Dados enviados automaticamente para o banco na nuvem via conexões seguras (SSL).  
- **Rastreabilidade:** Cada sensor possui um ID único para garantir a identificação.  

### 🔒 Segurança dos Dados:
- Conexão Criptografada (SSL) entre sensores e banco.  
- Autenticação segura com senha forte e controle de IP no AWS RDS.  
- Monitoramento contínuo para detectar acessos irregulares.  

---

## 6. 📋 Plano de Desenvolvimento (3 Membros)

| Membro   | Função                     | Tarefas                                                                  |
|---------|-----------------------------|--------------------------------------------------------------------------|
| Pedro   | Infraestrutura de Dados      | Configuração AWS RDS, integração ESP32, testes de conectividade            |
| Flavia  | Análise de Dados e IA        | Modelagem preditiva com TensorFlow, notebooks de análise                   |
| Felipe  | Documentação e Organização   | Estruturação do GitHub, documentação técnica, controle de versões          |

---

## 7. 📁 Estrutura Inicial do Repositório
fpf-enterprises-ml-solution/
├── /docs/ # Documentação técnica e diagramas
├── /data/ # Scripts para coleta de dados
├── /model/ # Notebooks de análise preditiva
├── /cloud/ # Scripts de configuração da nuvem (AWS)
├── /logs/ # Arquivos de log para monitoramento
├── requirements.txt # Dependências do Python
└── README.md # Documento principal do projeto

---

## 8. 💻 Como Executar o Código
1. **Clonar o Repositório:**
   ```bash
   git clone https://github.com/seu-usuario/fpf-enterprises-predictive-maintenance.git
   cd fpf-enterprises-predictive-maintenance

---

## 9. 🗓️ Histórico de Lançamento
### Versão 1.0.0 - 2025-05-08
- Implementação inicial: coleta, armazenamento e processamento de dados sensoriais.  
- Modelagem preditiva com TensorFlow.  
- Documentação e estrutura de pastas definidas.  

### Versão 1.1.0 - (Prevista)
- Dashboards interativos com Streamlit.  
- Automação com AWS Lambda para atualização de modelos.  
- Integração com novos tipos de sensores (ex: sensores de pressão).  

---

## ✅ Como Atualizar o Projeto
1. **Puxar as atualizações do repositório:**  
   ```bash
   git pull origin main



## 📋 Licença

<img style="height:22px!important;margin-left:3px;vertical-align:text-bottom;" src="https://mirrors.creativecommons.org/presskit/icons/cc.svg?ref=chooser-v1"><img style="height:22px!important;margin-left:3px;vertical-align:text-bottom;" src="https://mirrors.creativecommons.org/presskit/icons/by.svg?ref=chooser-v1"><p xmlns:cc="http://creativecommons.org/ns#" xmlns:dct="http://purl.org/dc/terms/"><a property="dct:title" rel="cc:attributionURL" href="https://github.com/agodoi/template">MODELO GIT FIAP</a> por <a rel="cc:attributionURL dct:creator" property="cc:attributionName" href="https://fiap.com.br">Fiap</a> está licenciado sobre <a href="http://creativecommons.org/licenses/by/4.0/?ref=chooser-v1" target="_blank" rel="license noopener noreferrer" style="display:inline-block;">Attribution 4.0 International</a>.</p>


