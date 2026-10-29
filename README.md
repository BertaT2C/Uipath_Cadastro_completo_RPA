# Cadastro automatizado a partir de planilha | UiPath RPA

**UiPath Studio · Excel · Interface web · Iteração por linhas · Automação de formulário**

## Visão geral

Este repositório contém um exercício de **automação de cadastro web a partir de uma planilha**. O projeto aparece como **“Aula3”** em `project.json`, e o fluxo `Main.xaml` combina leitura de dados em Excel com preenchimento de formulário no navegador.

**Objetivo do estudo:** demonstrar como dados estruturados de uma planilha podem orientar ações repetitivas de preenchimento de uma interface web.

> Os arquivos demonstram a configuração e a sequência do workflow. Não há aqui confirmação de cadastro efetivamente concluído, volume processado, taxa de sucesso ou execução em produção.

## Processo identificado no código

1. **Abrir e ler a planilha** utilizando atividades de Excel, incluindo **Read Range**.
2. **Percorrer os registros**, conforme a atividade **For Each Row in Data Table**.
3. **Interagir com um formulário web** em navegador **Edge**, identificado no workflow como **DesafioRPA**.
4. **Preencher campos** mapeados no fluxo: Nome, Logradouro, Cidade, Empresa, Cargo, Idade, Mãe, Pai e Salário.
5. **Interagir com opções do formulário** relacionadas a Estado e seleção indicada como Masculino.
6. Executar ações de interface nomeadas **Enviar** e **Enviar outra resposta**.

A lista descreve as atividades presentes; não comprova que cada registro foi aceito pelo formulário.

## Artefatos originais

| Arquivo | Finalidade |
| --- | --- |
| [`Main.xaml`](./Main.xaml) | Leitura do Excel, iteração, automação de interface e envio |
| [`project.json`](./project.json) | Configuração e dependências do UiPath |
| [`Desafio3.xlsx`](./Desafio3.xlsx) | Planilha existente no projeto, utilizada como fonte no exercício |

O projeto foi configurado em **UiPath Studio 21.10.5.0**, com **Visual Basic** e **framework Legacy**. O repositório mantém seus arquivos de automação sem alterações.

## Visão de Análise de Negócios

| Elemento | Questão funcional relevante |
| --- | --- |
| **Entrada** | Quais colunas da planilha são necessárias ao cadastro? |
| **Transformação** | Como os valores de cada linha são associados aos campos da tela? |
| **Regras** | Quais campos são obrigatórios e quais formatos são aceitos? |
| **Exceções** | Como lidar com registros incompletos, opções inválidas ou falha de navegação? |
| **Saída** | Como evidenciar que um registro foi efetivamente enviado e aceito? |

As perguntas representam **possibilidades de refinamento**, não requisitos confirmados.

## Cuidados para reprodução

O workflow depende da estrutura do arquivo Excel e da interface externa. Antes de executar, revise as referências, seletores e os dados do exercício. **Não utilize nem publique dados pessoais reais em formulários ou arquivos de demonstração sem autorização.**

## Evoluções possíveis — não implementadas neste README

- Validação dos dados antes do preenchimento;
- Registro de resultados por linha e tratamento de erro;
- Controle de duplicidade, tentativas e evidências de conclusão;
- Criação de massa de testes sintética e critérios de aceitação.

Este material mostra o **funcionamento lógico dos artefatos disponíveis** sem atribuir implantação ou resultados não evidenciados.
