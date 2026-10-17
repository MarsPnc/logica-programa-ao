# logica programaçao
# 🧮 Python Calculator & Automation Shell Script

Este repositório contém uma **calculadora básica desenvolvida em Python** e um **script Shell (Bash) para automatizar a sua execução** em ambientes Unix/Linux.

O objetivo deste projeto é fornecer uma ferramenta simples de linha de comando para operações matemáticas e demonstrar como scripts de terminal podem facilitar o fluxo de trabalho de desenvolvedores e administradores de sistemas.

---

## 🚀 Funcionalidades

### 1. Calculadora Python (`calculadora.py`)
A calculadora suporta as quatro operações matemáticas básicas:
* **Soma** (`+`)
* **Subtração** (`-`)
* **Multiplicação** (`*`)
* **Divisão** (`/`) — inclui validação para evitar a divisão por zero.

### 2. Script de Automação (`calculadora.sh`)
O script Shell automatiza as seguintes etapas:
* Verifica se o Python 3 está instalado no sistema.
* Define as permissões corretas de execução.
* Executa a calculadora automaticamente.
* Limpa o terminal antes e depois da execução para uma melhor experiência visual.

---

## 🛠️ Pré-requisitos

Antes de começares, certifica-te de que tens instalado no teu sistema:
* [Python 3.x](https://python.org)
* Terminal compatível com Bash (Linux, macOS ou WSL no Windows)

---

## 💻 Como Utilizar

### 1. Clonar o Repositório
```bash
git clone https://github.com
cd o-teu-repositorio
```

### 2. Execução Automatizada (Recomendado)
Para rodar o projeto usando o script de automação, basta dar permissão de execução ao ficheiro `.sh` e executá-lo:

```bash
chmod +x calculadora.sh
./calculadora.sh
```

### 3. Execução Manual (Apenas Python)
Se preferires correr a calculadora diretamente sem o script Shell:

```bash
python3 calculadora.py
```

---

## 📂 Estrutura do Código

### Ficheiro: `calculadora.py`
```python
def calcular():
    print("=== CALCULADORA PYTHON ===")
    try:
        num1 = float(input("Digite o primeiro número: "))
        operacao = input("Digite a operação (+, -, *, /): ")
        num2 = float(input("Digite o segundo número: "))

        if operacao == '+':
            resultado = num1 + num2
        elif operacao == '-':
            resultado = num1 - num2
        elif operacao == '*':
            resultado = num1 * num2
        elif operacao == '/':
            if num2 == 0:
                return "Erro: Divisão por zero não é permitida!"
            resultado = num1 / num2
        else:
            return "Operação inválida!"

        return f"Resultado: {resultado}"
    except ValueError:
        return "Erro: Por favor, insira apenas números válidos."

### Ficheiro: `calculadora.sh`
```bash
#!/bin/bash


# Executa o script Python
python3 calculadora.py


---

