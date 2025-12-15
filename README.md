# AES 3x3
```markdown
# Implementação Didática de Criptografia (Baseada em AES)

Este projeto consiste em uma implementação em linguagem C de um algoritmo de criptografia simétrica baseado na estrutura do **AES (Advanced Encryption Standard)**. O código demonstra o funcionamento interno das etapas de confusão e difusão utilizadas em criptografia moderna, adaptadas aqui para blocos de 9 bytes.

## 📋 Funcionalidades

O programa executa um fluxo completo de criptografia e descriptografia:

1.  **Encriptação:** Transforma a mensagem original ("Bom dia!!") em texto cifrado.
2.  **Gerenciamento de Arquivos:** Gera arquivos de texto contendo a mensagem original, a cifrada e a recuperada.
3.  **Descriptografia:** Realiza o processo inverso para recuperar a mensagem original.
4.  **Visualização Hexadecimal:** Exibe no console os valores dos bytes em cada etapa para fins de depuração.

## 🛠️ Como Funciona

O algoritmo segue a estrutura de rede de substituição-permutação (SP-network) característica do AES, operando sobre uma matriz de estado de 9 bytes (3x3). As etapas implementadas são:

* **SubBytes:** Substituição não-linear dos bytes usando uma S-Box (Rijndael S-box).
* **ShiftRows:** Permutação das linhas da matriz de estado para misturar os dados.
* **MixColumns:** Mistura os dados dentro de cada coluna usando aritmética de campos finitos (Multiplicação de Galois).
* **AddRoundKey:** Operação XOR entre o estado atual e a chave da rodada (`roundKey`).

Para a descriptografia, o código implementa as operações inversas (`InvSubBytes`, `InvShiftRows`, `InvMixColumns`).

## 🚀 Como Executar

### Pré-requisitos
* Compilador C (GCC, Clang ou MinGW).

### Compilação e Execução

No terminal, navegue até a pasta do projeto e execute:

```bash
# Compilar
gcc "AES código.c" -o aes_crypto

# Executar
./aes_crypto

```

##📂 Arquivos GeradosApós a execução, o programa criará os seguintes arquivos no diretório:

* `bomdia.txt`: Contém o texto plano original.
* `bomdiaCriptografado.txt`: Contém o resultado da encriptação (bytes ilegíveis).
* `bomdiaDescriptografado.txt`: Contém o texto recuperado após o processo de decriptação.

##⚠️ Aviso LegalEste código é uma **implementação educacional** destinada ao estudo de algoritmos criptográficos. Ele utiliza parâmetros fixos (chave e mensagem "hardcoded") e um tamanho de bloco não-padrão (9 bytes). **Não utilize este código para proteger dados sensíveis em produção.**

---

Desenvolvido para fins de estudo em Ciência da Computação.

```

```