# Projeto de Análise de Dados na Criação de Ovinos para Reprodução - EM CONSTRUÇÃO
<h4 align="center"> 
    :construction:  Projeto em construção  :construction:
</h4>
Esse projeto visa analisar o ciclo completo da criação de ovinos voltados para reprodução (*a princípio*), desde o nascimento até a destinação final.

## Estrutura do Projeto
### 1. Coleta de Dados
Dados sugeridos para coleta:
- Registro de nascimentos (*data, peso, sexo, mãe, pai*);
- Controle sanitário (*vacinas, medicamentos, doenças*);
- Desempenho de crescimento (*pesos periódicos*);
- Registro reprodutivo (*idade ao primeiro parto, taxa de concepção*);
- Destinação final (*venda para reprodução, descarte, óbitos*).

### 2. Modelagem de Dados
Serão criadas as seguintes tabelas relacionais:

- Tabela Animais

```
id_animal (chave primária e identificador único)
data_nascimento
sexo
peso_nascimento
id_mae
id_pai
tipo_parto
vivo
````

- Tabela Desmame
```
id_animal (chave estrangeira)
data_desmame
peso_desmame
idade_desmame
aprovado/ destino (atende pardrões reprodutivos) ???????
```

- Tabela Reprodutiva Fêmeas
```
id_animal (chave estrangeira)
data_primeiro_cio
data_primeiro_parto
num_partos
num_crias
intervalo_partos
crias_vivas_por_parto
```

- Tabela Reprodutiva Machos
```
id_animal (chave estrangeira)
data_avaliacao
circunferencia_escrotal
libido (escala de 1 - 5)
femeas_cobertas
femeas_prenhes
```

Tabela Sanitária

```
id_registro
id_animal (chave estrangeira)
tipo_evento (vacina/medicação/doença)
data_evento
descricao
observacoes
```

Tabela Gastos
```
id_registro
id_animal (chave estrangeira)
custo_evento
consumo_racao
custo_racao
```

### 3. Painéis de Análise (*Dashboards*)
- Painel 1: Desempenho Reprodutivo
  - Gráfico de taxa de concepção por reprodutor;
  - Média de crias por parto por ano;
  - Intervalo médio entre partos;
  - Idade média ao primeiro parto.

- Painel 2: Crescimento e Desenvolvimento
  - Curva de crescimento média por sexo;
  - Peso aos 60/90/180 dias;
  - Custo médio com alimentação por animal;
  - Comparativo de ganho de peso diário.

- Painel 3: Saúde do Rebanho
  - Frequência de ocorrências sanitárias;
  - Custo médio com saúde por animal;
  - Taxa de mortalidade por faixa etária.

- Painel 4: Destinação Final
  - Razões de descarte (idade, produtividade, saúde);
  - Idade média na destinação;
  - Proporção de animais vendidos para reprodução.

- Painel 5: Custos do rebanho

### 4. Indicadores-chave de Desempenho (*KPIs*) 

- Taxa de sobrevivência até desmame;
- Idade média ao primeiro parto (*dias*);
- Intervalo médio entre partos (*dias*);
- Taxa de concepção (*%*);
- Ganho médio diário de peso (*g/dia*);
- Gasto médio semanal (*R$/dia*)
- Taxa de descarte reprodutivo (*%*).
  
## Adicionais

### 5. Implementação no Power BI
Passos básicos:

Importe os dados (Excel, CSV ou banco de dados)

Crie relações entre as tabelas

Desenvolva medidas usando DAX para cálculos específicos

Crie visualizações interativas

Publique no Power BI Service (versão gratuita com limitações)

### 6. Análises Recomendadas
Correlação entre peso ao nascer e desempenho reprodutivo

Impacto da estação do ano nas taxas de concepção

Eficiência reprodutiva por linhagem/genética

Custo-benefício por matriz considerando vida produtiva

### 7. Dicas para Coleta de Dados
Utilize planilhas padronizadas no campo

Considere identificação individual (brincos eletrônicos)

Registre eventos imediatamente após ocorrência

Faça pesagens em intervalos regulares