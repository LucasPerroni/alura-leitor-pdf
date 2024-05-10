<p align="center">
  <h1 align="center">
    Leitor de vestibular
  </h1>
</p>

Projeto realizado para a imersão de IA da Alura. Grande parte da função ``extract_questions()`` foi gerada pelo Gemini, somente com alguns ajustes feitos por mim.

---
## 💻 Tecnologias utilizadas

- Google Colab
- Gemini
- Python
---
## 🏁 Como utilizar

- Abra o arquivo .ipynb no Google Colab
- Configure o "api_key" com a sua API Key do Google dentro do Secrets do Colab
- Faça upload do arquivo pdf dentro dos Arquivos do Colab
- Certifique-se de que o ``pdf_path`` está levando para o caminho do pdf
- Divirta-se ^-^
---
## ✨ Pontos de destaque
- Esse código cria uma variável chamada ``questions``. Essa variável é um JSON com todas as questões do vestibular, que pode ser utilizado em outros lugares caso haja o interesse.
- A função ``extract_questions()`` ainda não está perfeita. Entre os problemas dela, destaca-se a incapacidade de extrair todos os textos referência de múltiplas questões ao mesmo tempo. O código conseguiu pular alguns desses textos, mas outros acabaram parando na alternativa "e)" da questão anterior. Acredito que isso seja um problema do PyPDF2, que não foi capaz de identificar esses trechos no pdf. Essa função também não é capaz de pegar as imagens das questões.
- O usuário pode fazer mais perguntas para o modelo, só é preciso se atentar a formatação do prompt. Use como exemplo os dois prompts já presentes, que usam a f-string e fazem referência as questões como ``questions_data[_numero da questão - 1_]``.
