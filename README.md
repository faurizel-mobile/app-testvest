# TestVest

Aplicativo Android desenvolvido em Kotlin para simular a experiência de um app de estudos e preparação para vestibular. O projeto foi estruturado com telas simples em XML e navegação entre atividades, ideal para uso em aula de desenvolvimento mobile.

## Visão geral

O app apresenta uma proposta de fluxo inicial:

- Tela principal de apresentação
- Tela de login
- Tela inicial do app com menu de ações
- Navegação entre atividades

A estrutura atual do projeto inclui:

- `app/src/main/java/com/example/simuladosdevestibularenem/MainActivity.kt`
- `app/src/main/java/com/example/simuladosdevestibularenem/LoginActivity.kt`
- `app/src/main/java/com/example/simuladosdevestibularenem/HomeActivity.kt`
- `app/src/main/res/layout/activity_main.xml`
- `app/src/main/res/layout/activity_login.xml`
- `app/src/main/res/layout/activity_home.xml`

## Objetivo do projeto

O objetivo deste app é demonstrar:

- criação de telas em Android com XML
- uso de `AppCompatActivity`
- navegação entre telas com `Intent`
- organização de layouts e recursos do Android
- desenvolvimento de um protótipo funcional para aula prática

## Tecnologias utilizadas

- Kotlin
- Android Studio
- Material Components
- ConstraintLayout
- XML para definição das telas

## Fluxo do app

O fluxo principal do projeto é:

1. A aplicação inicia em `MainActivity`
2. O botão de login navega para `HomeActivity`
3. Há também a tela `LoginActivity` para representação de autenticação
4. A tela inicial do app oferece ações como:
   - Iniciar Simulado
   - Ver desempenho
   - Configurações
   - Acesso a matérias

## Mockup do app

A seguir, um mockup simplificado da interface proposta:

```text
+-----------------------------------------------+
|                     TestVest                   |
|       Prepare-se para o vestibular!          |
|                                               |
|  [Digite seu e-mail]                          |
|  [Digite sua senha]                           |
|                                               |
|                 [Entrar]                      |
|                Criar conta                    |
+-----------------------------------------------+

+-----------------------------------------------+
|                     TestVest                   |
|      Estude. Supere. Pratique.               |
|                                               |
|             [Iniciar Simulado]                |
|             [Ver desempenho]                  |
|             [Configurações]                   |
|                                               |
|                 Matérias                      |
|       [Mat]   [Física]   [Química]            |
+-----------------------------------------------+
```

## Estrutura da interface

### 1. Tela principal
A tela inicial do projeto utiliza `activity_main.xml` e representa a primeira interação do usuário, com campo de e-mail e botão para acessar o sistema.

### 2. Tela de login
A tela `activity_login.xml` contém:

- campo para e-mail
- campo para senha
- botão de entrada
- link para criar conta
- ícone de biblioteca

### 3. Tela inicial (Home)
A tela `activity_home.xml` contém:

- título do app
- mensagem motivacional
- botão de início do simulado
- opções de desempenho e configurações
- seção de matérias

## Procedimento didático para a aula

Abaixo está um guia passo a passo para conduzir a aula de forma prática e didática.

### Objetivo da aula
Ensinar os alunos a criar um aplicativo Android básico com navegação entre telas, usando layouts em XML e Kotlin.

### Tempo sugerido
45 a 90 minutos

### Materiais necessários

- Android Studio
- JDK instalado
- Emulador Android ou dispositivo físico
- Conhecimento básico de Kotlin e XML

### Passo 1: Apresentação do projeto
Explique que o app simula um ambiente de estudo para vestibulandos e que o objetivo é mostrar como uma aplicação pode organizar telas, ações e navegação.

Discuta rapidamente os componentes utilizados:

- `TextInputLayout`
- `TextInputEditText`
- `Button`
- `ImageView`
- `ConstraintLayout`

### Passo 2: Exploração do código
Mostre a estrutura do projeto e destaque os arquivos principais:

- `MainActivity.kt`: ponto de entrada da aplicação
- `LoginActivity.kt`: tela de autenticação
- `HomeActivity.kt`: tela inicial
- `activity_main.xml`, `activity_login.xml`, `activity_home.xml`: telas em XML

### Passo 3: Explicação da navegação
No código de `MainActivity.kt`, o botão realiza navegação usando `Intent`:

```kotlin
val intent = Intent(this, HomeActivity::class.java)
startActivity(intent)
```

Explique que:

- `Intent` serve para abrir outra tela
- `this` representa a Activity atual
- `HomeActivity::class.java` define a próxima tela

### Passo 4: Execução do app
No Android Studio:

1. Abra o projeto
2. Aguarde o Gradle sincronizar
3. Selecione um emulador ou dispositivo
4. Clique em "Run 'app'"
5. Observe a tela inicial

### Passo 5: Demonstrar o fluxo visual
Mostre aos alunos que o app possui:

- uma tela inicial com campo de e-mail
- acesso rápido a navegação
- uma tela de home com opções de estudo

### Passo 6: Identificação de componentes
Peça para os alunos localizarem no XML:

- ao menos um `Button`
- um `TextView`
- um `ImageView`
- um `TextInputLayout`

### Passo 7: Proposta de melhoria em grupo
Sugira desafios para a turma, por exemplo:

- criar validação de e-mail e senha
- adicionar botão para voltar
- incluir menu de matérias com ícones
- criar uma tela de desempenho
- implementar splash screen

### Passo 8: Exercício prático
Peça que os alunos:

1. alterem o texto do botão principal
2. criem uma nova tela para "Simulado"
3. adicionem um ícone ou imagem nova
4. conectem a nova tela via `Intent`

### Passo 9: discussão final
Conclua explicando que esse projeto funciona como base para apps reais de educação, educação financeira, gestão, entre outros. A lógica aprendida pode ser reaproveitada em outros projetos.

## Sugestão de extensão para o projeto

Para evoluir o app, os alunos podem implementar:

- autenticação com Firebase
- armazenamento de dados em banco local
- cálculo de desempenho
- tela de histórico de simulados
- animações e temas
- navegação por fragments

## Como rodar o projeto

1. Clone o repositório
2. Abra no Android Studio
3. Sincronize Gradle
4. Execute no emulador ou dispositivo

```bash
git clone https://github.com/faurizel-mobile/app-testvest.git
cd app-testvest
./gradlew assembleDebug
```

## Conclusão

Este app é um excelente exemplo para ensinar desenvolvimento Android mobile com Kotlin, pois combina:

- estrutura de projeto Android
- uso de interfaces em XML
- navegação entre telas
- lógica simples com Kotlin
- foco em didática e aprendizado prático

Se quiser, posso também criar uma versão mais sofisticada do README com:

- imagem de logo
- badges do projeto
- vídeo de demonstração
- instruções específicas para aula em laboratório
- uma documentação de arquitetura com diagramas

Ou posso adaptar esse README para um formato mais institucional, acadêmico ou para apresentação em sala de aula.
