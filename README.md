⭐ Modelagem Dimensional – Star Schema (Universidade)
📚 Descrição do Projeto

Este projeto apresenta a criação de um modelo dimensional utilizando o padrão Star Schema, desenvolvido a partir de um modelo relacional de uma universidade.

O objetivo é estruturar os dados para análise de informações relacionadas aos professores, permitindo consultas analíticas mais eficientes em ambientes de Business Intelligence (BI).

O modelo foi desenvolvido como parte de um desafio de modelagem de dados, no qual foi necessário transformar um banco relacional em um modelo dimensional.

🎯 Objetivo

Construir um Star Schema com foco na análise de dados de professores, considerando:

Disciplinas ministradas

Cursos relacionados

Departamentos

Datas de oferta

O modelo foi estruturado de forma que a tabela fato centralize os eventos relacionados aos professores, enquanto as tabelas dimensão armazenam os detalhes descritivos.

⭐ Estrutura do Star Schema

O modelo dimensional é composto por:

📊 Tabela Fato
FATO_PROFESSOR

Tabela responsável por armazenar os eventos e métricas relacionadas aos professores.

Possíveis campos:

idFatoProfessor (PK)

idProfessor (FK)

idDisciplina (FK)

idCurso (FK)

idDepartamento (FK)

idData (FK)

quantidadeDisciplinas

cargaHoraria

Esta tabela representa o evento de um professor ministrando uma disciplina em um determinado curso e período.

📦 Tabelas Dimensão
👨‍🏫 DIM_PROFESSOR

Armazena informações descritivas dos professores.

Campos exemplo:

idProfessor (PK)

nomeProfessor

titulacao

tempoCasa

departamento

📚 DIM_DISCIPLINA

Contém os detalhes das disciplinas.

Campos exemplo:

idDisciplina (PK)

nomeDisciplina

cargaHoraria

tipoDisciplina

🎓 DIM_CURSO

Informações relacionadas aos cursos.

Campos exemplo:

idCurso (PK)

nomeCurso

nivelCurso

modalidade

🏢 DIM_DEPARTAMENTO

Contém os departamentos da universidade.

Campos exemplo:

idDepartamento (PK)

nomeDepartamento

campus

📅 DIM_TEMPO

Dimensão criada para possibilitar análises temporais, já que o modelo relacional original não possuía dados de data.

Campos exemplo:

idData (PK)

dataCompleta

dia

mes

nomeMes

trimestre

semestre

ano

diaSemana

🔎 Granularidade do Modelo

A granularidade adotada foi:

Um registro na tabela fato representa um professor ministrando uma disciplina em um curso em uma determinada data.

Essa granularidade permite análises como:

Quantidade de disciplinas ministradas por professor

Professores por departamento

Disciplinas oferecidas por curso

Análise temporal das ofertas


🛠 Ferramentas Utilizadas

MySQL Workbench

Modelagem Dimensional

Star Schema

Banco de Dados Relacional

📊 Benefícios do Modelo Dimensional

A utilização do Star Schema proporciona:

Melhor desempenho em consultas analíticas

Estrutura simples para ferramentas de BI

Facilidade na criação de dashboards

Maior organização dos dados para análise
