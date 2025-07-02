# 🔎 Análise de Pacote HTTP com Wireshark

Este projeto demonstra uma análise técnica de uma requisição HTTP capturada com o Wireshark em um ambiente controlado. A atividade foca no entendimento do protocolo HTTP (versão 1.1) através da observação prática de pacotes gerados por um servidor local.

---

## 🚀 Objetivo

- Compreender o funcionamento de requisições e respostas HTTP
- Utilizar o Wireshark para filtrar e inspecionar pacotes de rede
- Visualizar o protocolo HTTP na prática em ambiente local
- Desenvolver documentação técnica para projetos de cibersegurança

---

## 🔧 Tecnologias Utilizadas

- [Wireshark](https://www.wireshark.org/) – captura e análise de pacotes
- [Python 3](https://www.python.org/) – servidor HTTP local
- Navegador Web (Firefox)
- Sistema Linux (Parrot OS)

---

## 📦 Estrutura do Projeto

```
analise-http-wireshark/
├── analise.md          # Documento técnico da análise
├── README.md           # Apresentação do projeto
└── imagens/            # Evidências visuais (prints)
    ├── get-request.jpg
    └── http-200-ok.jpg
```

---

## 🔢 Como Reproduzir o Experimento

### 1. Iniciar servidor HTTP local

```bash
python3 -m http.server 8000
```

### 2. Abrir o Wireshark

- Iniciar captura na interface `lo` (loopback)
- Aplicar filtro:

```wireshark
http
```

ou

```wireshark
tcp.port == 8000
```

### 3. Acessar no navegador

```
http://localhost:8000
```

### 4. Parar a captura e analisar:

- Localize pacotes:
  - `GET / HTTP/1.1`
  - `HTTP/1.1 200 OK`
- Clique com o botão direito → *Follow TCP Stream* para visualização completa

---

## 🧠 Resultado Esperado

O Wireshark deve exibir a troca de pacotes entre cliente e servidor:

- Requisição `GET` feita pelo navegador
- Resposta `200 OK` do servidor Python
- Headers HTTP visíveis e conteúdo HTML da listagem de diretórios

---

## 📂 Documentação

O arquivo [`analise.md`](./analise.md) contém:

- Detalhes do ambiente de teste
- Descrição dos pacotes analisados
- Prints da análise
- Conclusão técnica

---

## 👤 Autor

**Roger**  
Estudante de Cibersegurança | 2025  
