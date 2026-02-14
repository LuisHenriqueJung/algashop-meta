# algashop-meta

Meta-repositório do AlgaShop para orquestrar os microservices via Git submodules.

## 🚀 Tecnologias

- **Linguagem**: Java 21 (nos microservices)
- **Framework**: Spring Boot 4.0.1 (microsservices/ordering)
- **Banco de Dados**: Não configurado neste meta-repo (ver cada microservice)
- **Autenticação**: Não aplicável neste meta-repo (ver cada microservice)
- **Build**: Gradle (Wrapper) 9.2.1
- **Contêinerização**: Não aplicável neste meta-repo
- **Gerenciamento de código**: Git Submodules

## 📋 Requisitos

- Git 2.x
- Java 21 (para build/execução dos microservices Java)
- Acesso aos repositórios remotos dos submodules

## ⚙️ Configuração

1. **Checkout do meta-repo com submodules**:
   - Clone trazendo os submodules automaticamente.
   ```bash
   git clone --recurse-submodules https://github.com/LuisHenriqueJung/algashop-meta.git
   ```

2. **Atualizar/Inicializar submodules (se você já clonou sem recurse)**:
   - Inicialize e atualize todos os submodules.
   ```bash
   git submodule update --init --recursive
   ```

## 🚀 Executando o Projeto

### Localmente
```bash
# Exemplo (Windows/PowerShell): executar o microservice ordering
cd microsservices/ordering
.\\gradlew.bat bootRun
```

### Com Docker
```bash
# Não há docker-compose/Dockerfile neste meta-repo.
# Verifique se cada microservice possui configuração Docker própria.
```

## 📚 Estrutura do Projeto

```
algashop-meta/
├── microsservices/
│   ├── ordering/    # Microservice de pedidos (submodule)
│   └── docs/        # Documentação do projeto (submodule)
└── .gitmodules      # Mapeamento de submodules
```

## 🔒 Autenticação

Não aplicável neste meta-repo.

## 📄 Documentação

- **Docs (submodule)**: `microsservices/docs`

## 🛠️ Desenvolvimento

### Build
```bash
# Exemplo: build do microservice ordering
cd microsservices/ordering
.\\gradlew.bat build
```

### Testes
```bash
# Exemplo: testes do microservice ordering
cd microsservices/ordering
.\\gradlew.bat test
```

---

Desenvolvido por RSData - 2026
