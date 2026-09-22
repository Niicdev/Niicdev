name: Generate Snake

on:
  schedule:
    - cron: "0 */6 * * *"   # roda automaticamente a cada 6 horas
  workflow_dispatch:         # permite rodar manualmente pelo botão "Run workflow"
  push:
    branches:
      - main

jobs:
  build:
    runs-on: ubuntu-latest
    permissions:
      contents: write
    steps:
      - uses: actions/checkout@v4

      - name: Generate snake animation
        uses: Platane/snk@v3
        id: snake-gif
        with:
          github_user_name: ${{ github.repository_owner }}
          outputs: |
            dist/github-contribution-grid-snake.svg
            dist/github-contribution-grid-snake-dark.svg?palette=github-dark

      - name: Push snake svg to the output branch
        uses: crazy-max/ghaction-github-pages@v4
        with:
          target_branch: output
          build_dir: dist
        env:
          GITHUB_TOKEN: ${{ secrets.GITHUB_TOKEN }}
### Conecte-se comigo
[![Instagram](https://img.shields.io/badge/-Instagram-C9A0DC?style=for-the-badge&logo=instagram&logoColor=white)](https://instagram.com/niccoding)
Building useful things and learning in public.

- 👥 **1** followers · **1** following

## Proof at a glance

<table>
<tr><td align="center"><b>1</b><br/><sub>repos</sub></td><td align="center"><b>0</b><br/><sub>stars</sub></td><td align="center"><b>11</b><br/><sub>contributions</sub></td></tr>
</table>

## Core toolkit

No public language data yet — building the first project in the open.

## Selected work

- **[Niicdev](https://github.com/Niicdev/Niicdev)** — Featured public work · ⭐ 0

## Let’s connect

<p align="center">
  <img src="https://www.gitskins.com/api/section/social?username=niicdev&theme=github-dark&avatar=https%3A%2F%2Favatars.githubusercontent.com%2Fu%2F317420921%3Fu%3Dbbf14bffb96af5dc9292f5081c72b28427c74e41%26v%3D4" alt="niicdev social visual" />
</p>

<a href="https://github.com/niicdev">GitHub</a>

<p align="center"><sub>niicdev · Recruiter-ready profile generated with <a href="https://www.gitskins.com/readme-generator">GitSkins</a></sub></p>
