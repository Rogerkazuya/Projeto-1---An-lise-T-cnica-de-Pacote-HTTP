# 📊 Análise Técnica: Pacote HTTP com Wireshark

Este documento detalha a análise de uma requisição HTTP capturada com o Wireshark, utilizando um servidor local em Python para fins educacionais.

---

## ⚙️ Ambiente de Teste

- **Sistema Operacional:** Parrot OS
- **Servidor HTTP:** Python 3 (`python3 -m http.server 8000`)
- **Navegador:** Firefox
- **Captura de Pacotes:** Wireshark
- **Interface de rede:** `lo` (loopback)

---

## 🔁 Descrição da Comunicação

### 📡 Requisição HTTP

- **Protocolo:** HTTP/1.1  
- **Método:** `GET`  
- **Host:** `localhost:8000`  
- **Path:** `/`  
- **IP de origem/destino:** `127.0.0.1`  
- **Porta de origem:** 42014 *(aleatória)*  
- **Porta de destino:** 8000 *(servidor HTTP local)*

📸 **Print:** `img1.jpg`

---

### 📦 Resposta HTTP

- **Status:** `HTTP/1.1 200 OK`
- **Conteúdo retornado:** Listagem de diretório (index padrão do Python server)
- **Tamanho:** 3589 bytes
- **Headers importantes:**
  - `Content-Type: text/html`
  - `Content-Length: ...`

📸 **Print:** `HTTP.1.1 200.jpg`

---

## 🧠 Análise Técnica

- O pacote `GET` demonstra o início de uma requisição do navegador.
- O pacote `200 OK` mostra que o servidor respondeu com sucesso.
- O tráfego ocorreu **totalmente localmente (127.0.0.1)**.
- Foi utilizado o protocolo **HTTP sobre TCP** (não criptografado).

---

## 📚 Conclusão

Esta análise é útil para iniciantes compreenderem o básico do protocolo HTTP, o processo de requisição e resposta, além de aprenderem a utilizar filtros e explorar pacotes no Wireshark.

---

## 📁 Evidências Visuais

- `imagens/img1.jpg`
- `imagens/HTTP.1.1 200.jpg`

---

## 🧑‍💻 Autor

**Roger**  
Estudante de Cibersegurança | 2025  
