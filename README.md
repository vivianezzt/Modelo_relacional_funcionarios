# Formação Desenvolvedor Moderno
## Módulo: Banco de Dados
## Capítulo: Modelo Lógico Relacional

# DESAFIO: Modelo Relacional Funcionários

<p>A partir da visão geral do sistema, do modelo conceitual e sua instância, elabore a especificação textual equivalente do modelo relacional, bem como uma representação gráfica da instância dos dados na forma de tabelas.</p>

### VISÃO GERAL DO SISTEMA: 
<p>Deseja-se fazer um sistema para registrar os funcionários de uma empresa, bem como as empreitadas às quais eles são atribuídos ao longo do tempo. Cada funcionário possui nome e e-mail, e pode pertencer a um ou mais departamentos. Cada empreitada possui uma data de início e de fim, e pode ter vários funcionários atribuídos a ela, sendo que cada atribuição de um funcionário em uma empreitada deve armazenar a quantidade de horas que o funcionário vai trabalhar na empreitada, bem como o valor por hora que o funcionário vai ganhar. Cada empreitada é contratada por uma empresa contratante, que possui nome e telefone.</p>

<img src="https://github.com/vivianezzt/Modelo_relacional_funcionarios/blob/main/funcionario_1.png">

### Instância:

<img src="https://github.com/vivianezzt/Modelo_relacional_funcionarios/blob/main/funcionario_2.png">

## Resolução: 

```
tb_funcionarios (id, nome, email)
tb_departamentos (id, nome)
tb_funcionarios_departamentos (id_funcionario, id_departamento)
	id_funcionarios referencia tb_funcionarios
	id_departamento referencia tb_departamento
tb_empreitada (id, id_contratante, dataInicio, dataFim)
	id_contratante referencia tb_contratante
tb_contratante (id, nome, telefone)
tb_atribuicoes (id, id_funcionario, id_empreitada, quantidadeHoras, valorPorHora)
	id_funcionario referencia tb_funcionarios
	id_empreitada referencia tb_empreitada
```

### Modelo Realacional: 

### Tabela Departamento
<img src="https://github.com/vivianezzt/Modelo_relacional_funcionarios/blob/main/tb_departamento.png">

### Tabela Funcionários
<img src="https://github.com/vivianezzt/Modelo_relacional_funcionarios/blob/main/tb_funcionarios.png">

### Tabela Atribuições
<img src="https://github.com/vivianezzt/Modelo_relacional_funcionarios/blob/main/tb_atribuicoes.png">

### Tabela Funcionários Departamentos
<img src="https://github.com/vivianezzt/Modelo_relacional_funcionarios/blob/main/funcionarios_departamentos.png">

### Tabela Empreitadas
<img src="https://github.com/vivianezzt/Modelo_relacional_funcionarios/blob/main/tb_empreitadas.png">

### Tabela Contratantes
<img src="https://github.com/vivianezzt/Modelo_relacional_funcionarios/blob/main/tb_contratantes.png">


<h3> CRÉDITOS &copy;</h3>
<h4> Este desafio foi proposto pelo Prof. <a href="https://www.instagram.com/devsuperior.ig/">Nélio Alves</a> no Módulo - Programação Moderna (JAVA)
</h4><a href="https://devsuperior.com.br/evento-sds">DEVSUPERIOR - Faça parte você támbem</a>
