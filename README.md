
Typing SVG
viewsfollowersstars
🧑‍🚀 About Me
name: Aadhithyanborn: 2006role: Student Developerlocation: Indiacurrent_focus: ["Web Development", "DSA", "Open Source"]learning: ["React", "Node.js", "Python"]fun_fact: "I debug with console.log and pray 🙏"
🔭 I'm currently working on [your project name]
🌱 I'm currently learning [what you're learning]
👯 Looking to collaborate on open source & fun side projects
💬 Ask me about anything — I love tech talks!
⚡ Fun fact: [something unique about you]
⚙️ Tech Stack
👨‍💻 Languages
PythonJavaScriptJavaHTML5CSS3

🖥️ Frameworks & Tools
ReactNode.jsGitVS CodeMySQL

📊 GitHub Stats



🌐 Connect With Me

🐍 Snake Animation
Snake animation

⚙️ File 2: .github/workflows/snake.yml
This makes the snake animation work. In your profile repo, create the folder .github/workflows/ and add this file:

yaml

name: Generate Snake

on:
  schedule:
    - cron: "0 0 * * *"
  workflow_dispatch:

jobs:
  build:
    runs-on: ubuntu-latest
    permissions:
      contents: write
    steps:
      - name: Generate Snake
        uses: Platane/snk@v3
        with:
          github_user_name: Aadhithyan2006
          outputs: |
            dist/github-snake.svg
            dist/github-snake-dark.svg?palette=github-dark

      - name: Push to output branch
        uses: crazy-max/ghaction-github-pages@v4
        with:
          target_branch: output
          build_dir: dist
        env:
        
