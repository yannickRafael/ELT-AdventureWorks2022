# **Análise de Dados: Satisfação de Clientes com Lógica Fuzzy**
Este projeto realiza a análise de dados da base [**AdventureWorks2022**](https://learn.microsoft.com/en-us/sql/samples/adventureworks-install-configure?view=sql-server-ver16&tabs=ssms) com o objetivo de medir e compreender a **satisfação do cliente** utilizando a **lógica fuzzy**. A abordagem combina modelagem de dados multidimensional, análise fuzzy e técnicas de aprendizado de máquina.



## **Descrição do Projeto**
O projeto foi desenvolvido como parte de uma atividade prática e inclui os seguintes componentes:
1. **Modelagem em Star Schema**: Construção de um esquema em estrela para organizar os dados.
2. **Transformação e Tratamento**: Limpeza de dados e criação de métricas relacionadas à produção, descartes e localização.
3. **Relatórios e Visualizações**: Uso de ferramentas como **Power BI** para apresentar resultados.
4. **Análise Fuzzy**: Aplicação da lógica fuzzy para medir a satisfação do cliente com base em critérios como tempo de entrega, descontos e frequência de compras.
5. **Machine Learning**: Implementação de uma árvore de decisão para identificar causas de descartes de produtos.

Ferramentas usadas: Microsoft SQL Server, SSIS para automação de pipeline usando Microsoft Studio e Power BI.

## **Objetivos**
1. Modelar o **nível de produção** mensal, semestral e anual.
2. Quantificar artigos produzidos e descartados.
3. Identificar locais com maior incidência de descartes.
4. Analisar **satisfação do cliente** com lógica fuzzy.
5. Treinar um modelo de aprendizado de máquina para prever causas de descartes.

---

## **Estrutura do Projeto**
```
/src
  ├── data/
  │   ├── raw/         # Dados brutos extraídos da base AdventureWorks2022
  │   ├── cleaned/     # Dados tratados para análise
  ├── models/
  │   ├── star_schema.sql  # Código SQL para criar o star schema
  │   ├── fuzzy_analysis.py # Código Python para lógica fuzzy
  │   ├── decision_tree.py  # Modelo de árvore de decisão
/reports
  ├── PowerBI/          # Relatórios criados no Power BI
  ├── visualizations/   # Gráficos e insights
/documentation
  ├── slides/           # Apresentação Google Slides (anexada)
README.md
```
### **Star Schema**
![image](https://github.com/user-attachments/assets/6e6d87bb-617c-434d-ac47-29525985f574)

---

## **Como Executar**
### **Pré-requisitos**
- Python 3.8+
- Dependências listadas no arquivo `requirements.txt`
- Banco de dados SQL Server com a base **AdventureWorks2022**

### **Setup**
1. Clone o repositório:
   ```bash
   git clone https://github.com/seuusuario/adventureworks-fuzzy-analysis.git
   cd adventureworks-fuzzy-analysis
   ```
2. Instale as dependências:
   ```bash
   pip install -r requirements.txt
   ```
3. Configure a conexão com o banco no arquivo `config.py`.

4. Execute os scripts:
   - Para criar o **Star Schema**:
     ```bash
     python src/models/star_schema.sql
     ```
   - Para realizar a análise fuzzy:
     ```bash
     python src/models/fuzzy_analysis.py
     ```

---

## **Visualizações**
Os relatórios analíticos e gráficos foram criados no **Power BI**. As principais visualizações incluem:
1. **Produção Mensal, Semestral e Anual por Região**.
 ![image](https://github.com/user-attachments/assets/2806f2e8-7ccc-4c24-8fff-6aff4037d7b4)

2. **Artigos Produzidos e Descartados mensais (deve ter em conta que os produtos descartados são os que apresentam defeitos);**.
  ![image](https://github.com/user-attachments/assets/4fd4e131-857c-4da0-a95c-665f5d7953dd)

3. **Os locais onde verificam-se mais descartes de produtos.**.
![image](https://github.com/user-attachments/assets/d92b45cc-f700-4b46-ae55-cb6492af2cdf)


#  [Treinamento](https://github.com/yannickRafael/ELT-AdventureWorks2022/blob/Yannick/training_program.ipynb)
---

## **Contribuições**
Equipe:
- **Kelden Mourato**  
- **Mauro Mahassa**  
- **Yannick Matimbe**  
