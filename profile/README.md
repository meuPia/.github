# meuPiá

![meuPia logo](./meuPia.png)

### Democratizando a Engenharia de Software através do Portugol.

---

### 🚀 O Ecossistema

O **meuPiá** não é apenas um compilador, é uma plataforma completa que permite estudantes irem do "Olá Mundo" ao treinamento de Redes Neurais e controle de Foguetes, tudo em português.

| Módulo | Versão | Descrição | Status |
| --- | --- | --- | --- |
| [🧠 **Core**](https://github.com/meuPia/core) | `v1.2.0` | Transpilador Portugol → Python e gerenciador de pacotes (`mpgp`). | ✅ Estável |
| [🔬 **Lab**](https://github.com/meuPia/lab) | motor `v1.2.0` | IDE web que roda o Core no navegador (Pyodide + CodeMirror + Xterm.js). | ✅ Estável |
| [🏁 **Arena**](https://github.com/meuPia/arena) | `v0.1.0` | Plataforma para eventos de code challenge: desafios por equipe, correção automática com testes privados e placar em tempo real. | ✅ Beta |
| [🤖 **IA**](https://github.com/meuPia/ia) | `v0.1.0` | Treinamento de Machine Learning (Scikit-Learn) nativo. | ✅ Beta |
| [🔌 **Maker**](https://github.com/meuPia/maker) | `v0.1.0` | Transpilação para MicroPython (ESP32/Pico). | ✅ Beta |
| [🚀 **Espacial**](https://github.com/meuPia/espacial) | `v0.1.0` | Controle de telemetria para Kerbal Space Program. | ✅ Beta |
| [🗺️ **Grid**](https://github.com/meuPia/grid) | `v1.0.2` | Visualização de Grids 2D para algoritmos de busca (A*, BFS, DFS), com sensores do agente. | ✅ Estável |
| [🧪 **Testes**](https://github.com/meuPia/testes) | `v1.0.0` | Framework de testes automatizados e asserções. | ✅ Estável |
| [🎯 **Desafios**](https://github.com/meuPia/desafios) | `-` | Banco de dados estático (Git as DB) com 14 missões interativas. | ✅ Ativo |

### 🆕 Novidades

**Core 1.2.0: um compilador mais confiável**
- Uma auditoria encontrou e corrigiu 21 erros do compilador. Os testes agora também executam o Python gerado, em vez de só comparar texto.
- Expressões completas em comparações e laços: `se x + 1 > 0`, `para i de 0 ate n - 1`, passo negativo com limite inclusivo.
- Novos operadores `!=`, `%` e `mod`, e novos tipos `logico` e `lista` (`novo lista()`, `novo dicionario()`).
- Blocos vazios geram código válido, e a CLI sai com código de erro quando a compilação falha.
- Mensagens de erro com linha e coluna (`Erro léxico na linha 4, coluna 8: …`), que o Lab destaca direto no editor.

**Core 1.3.0 (em breve): variáveis locais**
- Declare variáveis dentro de `funcao`, `metodo` e `inicio`, com escopo próprio. Cada chamada (inclusive recursiva) tem as suas.

```portugol
funcao fatorial(n)
    var
        i: inteiro
        resultado: inteiro <- 1
    para i de 2 ate n faca
        resultado <- resultado * i
    fim_para
    retorne resultado
fim_funcao
```

**Lab**
- Já roda o `meupia-core` 1.2.0 em produção, com realce de sintaxe e marcação de erros no editor.

O Core e o Lab passaram a ser desenvolvidos com especificações [OpenSpec](https://github.com/Fission-AI/OpenSpec): cada mudança da linguagem nasce de uma spec com testes.

### 💻 IDE Online: Pratique Agora

Acesse o nosso ambiente de desenvolvimento direto do navegador: **[https://meupia-lab.vercel.app](https://meupia-lab.vercel.app)**
*(Dica: Para professores e alunos, é possível carregar exercícios específicos adicionando o parâmetro `?desafio=id_do_desafio` na URL!)*

### 🎯 Desafios Interativos (meuPiá-desafios)

O repositório **[meuPiá-desafios](https://github.com/meuPia/desafios)** atua como o banco de dados oficial de exercícios para o ecossistema (Git as a Database). Ele armazena missões estruturadas em arquivos `.json`, que são consumidas dinamicamente via CDN pela nossa IDE Online.

Cada desafio carrega as instruções do problema na tela e injeta testes unitários (da biblioteca `meuPia-testes`) de forma invisível no código do aluno, permitindo validar a lógica do aluno em tempo real.

As trilhas atuais cobrem Fundamentos de Inteligência Artificial:

| Trilha | Missões |
| --- | --- |
| 🧭 **Busca heurística e A*** | Radar do Motoboy (função sucessora), Taxímetro `g(n)`, Radar Manhattan e Euclidiano `h(n)`, Fila VIP, Memória Fotográfica, Fio de Ariadne, Fuga do Labirinto, Navegador A*, Entrega de Pizza Express |
| 🧩 **Representação do conhecimento** | Redes Semânticas, Frames (IF-ADDED / IF-NEEDED), Ontologias, Tradutor Universal (JSON-LD) |

Experimente: [meupia-lab.vercel.app/?desafio=a_estrela_manhattan](https://meupia-lab.vercel.app/?desafio=a_estrela_manhattan)

### 🏁 Competições (meuPiá-arena)

O **[meuPiá-arena](https://github.com/meuPia/arena)** é um fork do Lab adaptado para maratonas e eventos de code challenge. Cada equipe entra com seu código de acesso, resolve desafios na IDE do navegador e submete as soluções, que são corrigidas no servidor com testes públicos e privados.

- Desbloqueio progressivo de níveis e cooldown entre tentativas.
- Pontuação pela melhor submissão, com registro de quem escreveu cada solução.
- Placar em tempo real com modo telão e painel administrativo para a organização.
- Modo offline para eventos sem internet.

### 📦 Instalação Rápida

Comece instalando o núcleo do sistema, no seu terminal, execute:

```bash
pip install meupia-core
```

Instale as capacidades que você precisa:

```bash
# Para Ciência de Dados
mpgp instale ia

# Para Robótica e IoT
mpgp instale maker

# Para Algoritmos de Busca em Grafos
mpgp instale grid

# Para Testes Automatizados
mpgp instale testes
```

### 🗺️ Próximos Passos

- 📖 Guia completo da linguagem meuPiá.
- ✍️ Aceitar `função` / `fim_função` com acento, como já acontece com `então`, `senão` e `até`.
- 🔒 Testes ocultos nos desafios (`esperar_hash`), para validar a resposta sem revelar o valor esperado.
- 🧑‍🏫 Tutor Socrático e depuração "Time-Travel" no Lab.

### 🤝 Contribua

Somos um projeto Open Source focado em educação.
Participe das discussões ou abra um Pull Request em nossos repositórios!
