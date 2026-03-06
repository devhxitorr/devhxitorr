## Olá! Bem-vindo(a) ao meu lab de código. Sempre aprendendo e transformando ideias em soluções digitais. 🚀

name: Update README cards

on:
  schedule:
    - cron: "0 0 * * *" # Runs once daily at midnight
  workflow_dispatch:

jobs:
  build:
    runs-on: ubuntu-latest

    permissions:
      contents: write

    steps:
      - uses: actions/checkout@v6

      - name: Generate stats card
        uses: readme-tools/github-readme-stats-action@v1
        with:
          card: stats
          options: username=${{ github.repository_owner }}&show_icons=true
          path: profile/stats.svg
          token: ${{ secrets.GITHUB_TOKEN }}

      - name: Generate top languages card
        uses: readme-tools/github-readme-stats-action@v1
        with:
          card: top-langs
          options: username=${{ github.repository_owner }}&layout=compact&langs_count=6
          path: profile/top-langs.svg
          token: ${{ secrets.GITHUB_TOKEN }}

      - name: Generate pin card
        uses: readme-tools/github-readme-stats-action@v1
        with:
          card: pin
          options: username=readme-tools&repo=github-readme-stats
          path: profile/pin-readme-tools-github-readme-stats.svg
          token: ${{ secrets.GITHUB_TOKEN }}

      - name: Commit cards
        run: |
          git config user.name "github-actions[bot]"
          git config user.email "41898282+github-actions[bot]@users.noreply.github.com"
          git add profile/*.svg
          git commit -m "Update README cards" || exit 0
          git push
<!--
**devhxitorr/devhxitorr** is a ✨ _special_ ✨ repository because its `README.md` (this file) appears on your GitHub profile.

Here are some ideas to get you started:

- 🔭 I’m currently working on ...
- 🌱 I’m currently learning ...
- 👯 I’m looking to collaborate on ...
- 🤔 I’m looking for help with ...
- 💬 Ask me about ...
- 📫 How to reach me: ...
- 😄 Pronouns: ...
- ⚡ Fun fact: ...
-->

## 🧪 Meus Laboratórios de Código
![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=for-the-badge&logo=html5&logoColor=white)
![CSS3](https://img.shields.io/badge/CSS3-1572B6?style=for-the-badge&logo=css3&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black)
![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white)

## 👨‍💻 Códigos que Pretendo Dominar
![Java](https://img.shields.io/badge/Java-007396?style=for-the-badge&logo=java&logoColor=white)
![Csharp](https://img.shields.io/badge/C%23-239120?style=for-the-badge&logo=c-sharp&logoColor=white)
![Go](https://img.shields.io/badge/Go-00ADD8?style=for-the-badge&logo=go&logoColor=white)
![C++](https://img.shields.io/badge/C%2B%2B-00599C?style=flat-square&logo=c%2B%2B&logoColor=white)

## Social Medias 💻
[![LinkedIn Badge](https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/heitor-mesquita-420410392)
[![Discord Badge](https://img.shields.io/badge/Discord-5865F2?style=for-the-badge&logo=discord&logoColor=white)](Hxitorr)
[![Instagram Badge](https://img.shields.io/badge/Instagram-E4405F?style=for-the-badge&logo=instagram&logoColor=white)](https://www.instagram.com/devhxitorr?igsh=a3Y2dmVleXdmZXhz&utm_source=qr)
