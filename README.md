## Olá! Eu sou a Larissa Mourão 

- 🔭 Hoje sou estudante de Engenharia de Software 
- 🌱 I’m currently learning ...
- pronouns: ela/dela
  
<div>
  <a href="https://beacons.ai/larissamourrao">
    <img height="180em" src="https://github-readme-stats.vercel.app/api?username=larissamourrao&show_icons=true&theme=dracula&include_all_commits=falsi&count_private=true"/>
    <img height="180em" src="https://github-readme-stats.vercel.app/api/top-langs/?username=larissamourrao&layout=compact&langs_count=16&theme=dracula"/>
  </a>
</div>

<div style="display: inline_block"><br>
  <img align="center" alt="larissa-Python" height="30" width="40" src="https://raw.githubusercontent.com/devicons/devicon/master/icons/python/python-original.svg">
</div>

##

<div>

  <a href="https://instagram.com/larissamourrao" target="_blank">
    <img src="https://img.shields.io/badge/-Instagram-%23E4405F?style=for-the-badge&logo=instagram&logoColor=white" target="_blank">
  </a>

  <a href="mailto:contato@larissageovanna592@gmail.com">
    <img src="https://img.shields.io/badge/-Gmail-%23333333?style=for-the-badge&logo=gmail&logoColor=white" target="_blank">
  </a>

  <a href="https://www.linkedin.com/in/larissa-mourão-3546063a4/" target="_blank">
    <img src="https://img.shields.io/badge/-LinkedIn-%230077B5?style=for-the-badge&logo=linkedin&logoColor=white" target="_blank">
  </a>
</div>

name: Generate Datas

on:
  schedule: # execute every 12 hours
    - cron: "* */12 * * *"
  workflow_dispatch:

jobs:
  build:
    name: Jobs to update datas
    runs-on: ubuntu-latest
    steps:
      # Snake Animation
      - uses: Platane/snk@master
        id: snake-gif
        with:
          github_user_name: <seu-usuario>
          svg_out_path: dist/github-contribution-grid-snake.svg

      - uses: crazy-max/ghaction-github-pages@v2.1.3
        with:
          target_branch: output
          build_dir: dist
        env:
          GITHUB_TOKEN: ${{ secrets.GITHUB_TOKEN }}
