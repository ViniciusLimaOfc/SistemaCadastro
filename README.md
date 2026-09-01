# SistemaCadastro

Sistema Java simples desenvolvido para a atividade prática de Controle de Versão e Gerenciamento de Mudanças com Git.

## Sobre o projeto

O sistema apresenta um menu no console com as opções de cadastrar, listar e (após a evolução via branch) excluir usuários. O foco da atividade não é a implementação das funcionalidades, e sim o versionamento do projeto com Git/GitHub.

## Como executar

```bash
javac src/SistemaCadastro.java -d out
java -cp out SistemaCadastro
```

## Histórico de versionamento

- Commit inicial na `main`: `FIX[1] - Criação da versão inicial do sistema`
- Branch `feature/cadastro`: `FEAT[1] - Adicionada opção de exclusão de usuário`
- Merge da `feature/cadastro` na `main`
- Tag `v1.1.0` criada após o merge

## Análise rápida

**1. Qual a finalidade de uma branch?**

Uma branch permite criar uma linha de desenvolvimento paralela e isolada da branch principal. Com ela, é possível desenvolver uma nova funcionalidade, corrigir um bug ou testar uma ideia sem interferir no código que já está estável na `main`. Só depois de pronta e validada, essa branch é integrada ao projeto principal.

**2. Qual a diferença entre commit e merge?**

Um **commit** é um registro de uma alteração feita no código em um determinado momento — é como uma "fotografia" do estado do projeto, acompanhada de uma mensagem explicando o que foi feito. Já o **merge** é a ação de unir o histórico de duas branches diferentes, trazendo para uma branch (geralmente a `main`) as alterações que foram feitas em outra (como a `feature/cadastro`).

**3. Por que é importante utilizar mensagens claras nos commits?**

Mensagens claras facilitam o entendimento do histórico do projeto por qualquer pessoa da equipe, tornam mais fácil localizar quando e por que uma mudança específica foi feita, ajudam na revisão de código e são essenciais para rastrear a origem de bugs ou reverter alterações específicas quando necessário.

**4. Por que o controle de versão é importante em equipes de desenvolvimento?**

Porque permite que várias pessoas trabalhem no mesmo projeto simultaneamente sem sobrescrever o trabalho umas das outras, mantém um histórico completo de todas as mudanças feitas, possibilita reverter para versões anteriores em caso de erro, facilita a revisão e integração de código por meio de branches e merges, e melhora a organização e a rastreabilidade do desenvolvimento.

**5. O que representa a versão 1.1.0 no contexto desta atividade?**

Representa uma evolução incremental do sistema após a versão inicial (1.0.0): a inclusão da funcionalidade de exclusão de usuário. O número `1.1.0` segue o padrão de versionamento semântico (MAJOR.MINOR.PATCH), em que o incremento no MINOR (de 1.0.0 para 1.1.0) indica que uma nova funcionalidade foi adicionada de forma compatível com a versão anterior, sem quebrar nada que já existia.

**6. Comandos Git para criar a tag via CLI**

```bash
# Criar uma tag anotada (recomendado, guarda autor, data e mensagem)
git tag -a v1.1.0 -m "Versão 1.1.0 - Inclusão da opção de exclusão de usuário"

# Enviar a tag para o repositório remoto no GitHub
git push origin v1.1.0
```
