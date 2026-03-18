# meuPiá

![meuPia logo](./meuPia.png)

### Democratizando a Engenharia de Software através do Portugol.

</div>

---

### 🚀 O Ecossistema

O **meuPiá** não é apenas um compilador, é uma plataforma completa que permite estudantes irem do "Olá Mundo" ao treinamento de Redes Neurais e controle de Foguetes, tudo em português.

| Módulo | Versão | Descrição | Status |
| --- | --- | --- | --- |
| [🧠 **Core**](https://github.com/meuPia/core) | `v1.1.4` | O compilador modular e gerenciador de pacotes (`mpgp`). | ✅ Estável |
| [🔬 **Lab**](https://github.com/meuPia/lab) | `v1.1.19` | Ambiente de Desenvolvimento Integrado (IDE) web via Wasm. | ✅ Estável |
| [🤖 **IA**](https://github.com/meuPia/ia) | `v0.1.0` | Treinamento de Machine Learning (Scikit-Learn) nativo. | ✅ Beta |
| [🔌 **Maker**](https://github.com/meuPia/maker) | `v0.1.0` | Transpilação para MicroPython (ESP32/Pico). | ✅ Beta |
| [🚀 **Espacial**](https://github.com/meuPia/espacial) | `v0.1.0` | Controle de telemetria para Kerbal Space Program. | ✅ Beta |
| [🗺️ **Grid**](https://github.com/meuPia/grid) | `v1.0.2` | Visualização de Grids 2D (A*, BFS, DFS). | ✅ Estável |
| [🧪 **Testes**](https://github.com/meuPia/testes) | `v1.0.0` | Framework de testes automatizados e asserções. | ✅ Estável |
| [🎯 **Desafios**](https://github.com/meuPia/desafios) | `-` | Banco de dados estático (Git as DB) com missões interativas. | ✅ Ativo |

### 💻 IDE Online: Pratique Agora

Acesse o nosso ambiente de desenvolvimento direto do navegador: **[https://meupia-lab.vercel.app](https://meupia-lab.vercel.app)**
*(Dica: Para professores e alunos, é possível carregar exercícios específicos adicionando o parâmetro `?desafio=id_do_desafio` na URL!)*

### 🎯 Desafios Interativos (meuPiá-desafios)

O repositório **[meuPiá-desafios](https://github.com/meuPia/desafios)** atua como o banco de dados oficial de exercícios para o ecossistema (Git as a Database). Ele armazena missões estruturadas em arquivos `.json`, que são consumidas dinamicamente via CDN pela nossa IDE Online. 

Cada desafio carrega as instruções do problema na tela e injeta testes unitários (da biblioteca `meuPia-testes`) de forma invisível no código, permitindo validar a lógica do aluno em tempo real, cobrindo desde a sintaxe básica até algoritmos de Pathfinding (como o A*).

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

### 🤝 Contribua

Somos um projeto Open Source focado em educação.
Participe das discussões ou abra um Pull Request em nossos repositórios!
