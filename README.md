### Oi, eu sou a Julia Pinheiro 😄

- 🔭 Estou em busca de uma oportunidade de estágio ou desenvolvedora júnior.
- 🌱 Atualmente estou estudando Typescript
- 📫 How to reach me:  julia.pinheirooliveira222@gmail.com ou WhatsApp (11) 98435-6347
- 😄 Pronouns: ela/dela/she/her

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
          github_user_name: rafaballerini
          svg_out_path: dist/github-contribution-grid-snake.svg

      - uses: crazy-max/ghaction-github-pages@v2.1.3
        with:
          target_branch: output
          build_dir: dist
        env:
          GITHUB_TOKEN: ${{ secrets.GITHUB_TOKEN }}
