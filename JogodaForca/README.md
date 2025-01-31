---

# 🚀 Projeto Jogo da Forca com Python  

🎯 **Objetivo:** Criar um jogo da forca simples utilizando a biblioteca `random` para sortear palavras de uma lista.  

## 🔧 Tecnologias Utilizadas  
📌 **Biblioteca:** `random`  

## 🏗️ Estrutura do Código  
1️⃣ **Importação da biblioteca**  
   - Importamos `random` para realizar o sorteio das palavras.  

2️⃣ **Função `escolher_palavra`**  
   - Criamos uma lista de palavras possíveis e utilizamos `random.choice` para selecionar uma palavra aleatoriamente.  

3️⃣ **Função `jogar_forca`**  
   - Definimos a variável `palavra`, chamando `escolher_palavra()`.  
   - Criamos listas para armazenar letras corretas e erradas.  
   - Inicializamos as variáveis `tentativas` (limite de erros) e `pontos` (perde 10 pontos a cada erro).  

4️⃣ **Lógica do jogo**  
   - Exibimos uma mensagem inicial ao usuário.  
   - Criamos a variável `palavra_secreta` com `_` para representar as letras ocultas.  
   - Utilizamos um loop `while` para processar as tentativas do jogador.  
   - Se a letra inserida estiver correta, adicionamos à lista `letras_corretas`, caso contrário, decrementamos `tentativas` e `pontos`.  
   - O jogo finaliza quando o usuário acerta todas as letras ou esgota as tentativas.  

5️⃣ **Execução**  
   - Chamamos a função `jogar_forca()` dentro do `main` para iniciar o jogo.  

💡 **Resumo:** Esse projeto é uma ótima forma de praticar manipulação de listas, controle de fluxo (`if`, `while`) e interação com o usuário em Python.  

🔗 Vamos trocar ideias! Como você implementaria melhorias nesse jogo?  

#Python #Desenvolvimento #LógicaDeProgramação #ProjetosComPython  

---
