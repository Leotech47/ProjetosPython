O código está bem estruturado e funcional, mas há alguns pontos de melhoria e pequenas correções a serem feitas:

### ✅ **O que está correto e funcionando bem?**  
✔️ Sorteia corretamente uma palavra da lista.  
✔️ Permite ao usuário tentar adivinhar letra por letra.  
✔️ Exibe a palavra parcialmente revelada com `_` para letras não adivinhadas.  
✔️ Controla tentativas restantes e pontos corretamente.  
✔️ Encerra o jogo quando o usuário acerta a palavra ou esgota as tentativas.  

---

### ⚠️ **Problemas encontrados e sugestões de melhoria**  

1️⃣ **Repetição de letras corretas na lista**  
- O código permite adicionar várias vezes a mesma letra em `letras_corretas`, mesmo que o usuário já tenha acertado essa letra antes.  
- **Correção:** Antes de adicionar `tentativa` em `letras_corretas`, verificar se a letra já está na lista.  

   **Correção sugerida:**  
   ```python
   if tentativa in palavra and tentativa not in letras_corretas:
       print("Letra correta!")
       letras_corretas.append(tentativa)
   ```

2️⃣ **Repetição de letras erradas na lista**  
- Se o usuário digitar uma letra errada mais de uma vez, o código conta como erro novamente e diminui o número de tentativas e pontos desnecessariamente.  
- **Correção:** Antes de adicionar `tentativa` em `letras_erradas`, verificar se a letra já foi tentada.  

   **Correção sugerida:**  
   ```python
   if tentativa not in letras_corretas and tentativa not in letras_erradas:
       if tentativa in palavra:
           print("Letra correta!")
           letras_corretas.append(tentativa)
       else:
           print("Letra errada! Tente novamente.")
           letras_erradas.append(tentativa)
           tentativas -= 1
           ponto -= 10
           print(f"Você tem {tentativas} tentativas restantes.")
   else:
       print("Você já tentou essa letra. Escolha outra.")
   ```

3️⃣ **Verificação de entrada vazia**  
- Se o usuário pressionar apenas "Enter" sem digitar nada, o código aceita isso como uma tentativa inválida.  
- **Correção:** Adicionar uma verificação para evitar entradas vazias.  

   **Correção sugerida:**  
   ```python
   if not tentativa.isalpha() or len(tentativa) != 1:
       print("Entrada inválida! Digite apenas uma letra.")
       continue
   ```

4️⃣ **Uso de letras maiúsculas e acentos**  
- O código já converte a entrada do usuário para minúsculas (`.lower()`), mas a lista de palavras pode conter palavras com acentos em alguns contextos.  
- **Solução:** Padronizar as palavras removendo acentos ou tratando palavras com caracteres especiais corretamente.

---

### 🎯 **Versão corrigida e melhorada**
Aqui está o código atualizado com as correções:

```python
import random

def escolher_palavra():
    palavras = ["python", "javascript", "frontend", "backend", "java"]
    return random.choice(palavras)

def jogar_forca():
    palavra = escolher_palavra()
    letras_corretas = []
    letras_erradas = []
    tentativas = 5
    ponto = 100

    print("Bem-vindo ao Jogo da Forca!")
    print("Adivinhe a palavra secreta.")

    while True:
        palavra_secreta = "".join([letra if letra in letras_corretas else "_" for letra in palavra])

        print("\nPalavra:", palavra_secreta)

        if palavra_secreta == palavra:
            print(f"Parabéns! Você acertou a palavra ({palavra}) com {ponto} pontos.")
            break

        tentativa = input("Digite uma letra: ").lower().strip()

        if not tentativa.isalpha() or len(tentativa) != 1:
            print("Entrada inválida! Digite apenas uma letra.")
            continue

        if tentativa in letras_corretas or tentativa in letras_erradas:
            print("Você já tentou essa letra. Escolha outra.")
            continue

        if tentativa in palavra:
            print("Letra correta!")
            letras_corretas.append(tentativa)
        else:
            print("Letra errada! Tente novamente.")
            letras_erradas.append(tentativa)
            tentativas -= 1
            ponto -= 10
            print(f"Você tem {tentativas} tentativas restantes.")

        if tentativas == 0:
            print("Você perdeu! A palavra era:", palavra)
            break

if __name__ == "__main__":
    jogar_forca()
```

---

### 🔥 **O que foi melhorado?**  
✅ **Evita adicionar letras repetidas nas listas de corretas e erradas**  
✅ **Impede tentativas vazias ou inválidas (números, caracteres especiais, espaço em branco)**  
✅ **Utiliza `.strip()` para remover espaços extras na entrada do usuário**  
✅ **Código mais organizado e eficiente com list comprehension (`palavra_secreta`)**  

Agora o jogo está mais robusto e evita comportamentos indesejados! 🚀
