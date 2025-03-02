# 👋 Hi there! I'm Karl Ancel Dimabayao  

I'm a passionate **student and developer** exploring the world of **web and mobile development**. I love learning new technologies and building innovative projects. 🚀  

---

## 📊 GitHub Stats  

<div align="center">
  <img src="https://github-readme-stats.vercel.app/api?username=karlanceldimabayao&hide_title=false&hide_rank=false&show_icons=true&include_all_commits=true&count_private=true&disable_animations=false&theme=dracula&locale=en&hide_border=false" height="150" alt="GitHub Stats" />
  <img src="https://github-readme-stats.vercel.app/api/top-langs?username=karlanceldimabayao&locale=en&hide_title=false&layout=compact&card_width=320&langs_count=5&theme=dracula&hide_border=false" height="150" alt="Top Languages" />
</div>

---

## 💻 Tech Stack  

<div align="left">
  <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/javascript/javascript-original.svg" height="30" alt="JavaScript" />
  <img width="12" />
  <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/typescript/typescript-original.svg" height="30" alt="TypeScript" />
  <img width="12" />
  <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/react/react-original.svg" height="30" alt="React" />
  <img width="12" />
  <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/html5/html5-original.svg" height="30" alt="HTML5" />
  <img width="12" />
  <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/css3/css3-original.svg" height="30" alt="CSS3" />
  <img width="12" />
  <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/python/python-original.svg" height="30" alt="Python" />
  <img width="12" />
  <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/csharp/csharp-original.svg" height="30" alt="C#" />
</div>

---

## 📱 Connect with Me  

<div align="left">
  <a href="https://www.youtube.com" target="_blank">
    <img src="https://img.shields.io/static/v1?message=YouTube&logo=youtube&label=&color=FF0000&logoColor=white&labelColor=&style=for-the-badge" height="35" alt="YouTube" />
  </a>
  <a href="https://www.instagram.com" target="_blank">
    <img src="https://img.shields.io/static/v1?message=Instagram&logo=instagram&label=&color=E4405F&logoColor=white&labelColor=&style=for-the-badge" height="35" alt="Instagram" />
  </a>
  <a href="https://www.twitch.tv" target="_blank">
    <img src="https://img.shields.io/static/v1?message=Twitch&logo=twitch&label=&color=9146FF&logoColor=white&labelColor=&style=for-the-badge" height="35" alt="Twitch" />
  </a>
  <a href="https://discord.com" target="_blank">
    <img src="https://img.shields.io/static/v1?message=Discord&logo=discord&label=&color=7289DA&logoColor=white&labelColor=&style=for-the-badge" height="35" alt="Discord" />
  </a>
  <a href="mailto:zenn.studio.01@gmail.com">
    <img src="https://img.shields.io/static/v1?message=Gmail&logo=gmail&label=&color=D14836&logoColor=white&labelColor=&style=for-the-badge" height="35" alt="Gmail" />
  </a>
  <a href="https://www.linkedin.com" target="_blank">
    <img src="https://img.shields.io/static/v1?message=LinkedIn&logo=linkedin&label=&color=0077B5&logoColor=white&labelColor=&style=for-the-badge" height="35" alt="LinkedIn" />
  </a>
</div>

---

## 🐍 Snake Animation  

![Snake animation](https://github.com/karlanceldimabayao/karlanceldimabayao/blob/output/github-contribution-grid-snake.svg)  

---

## 🔥 Fun Fact  
💡 I'm always curious about new technologies and love experimenting with different programming languages!  

---

### 🚀 **How to Make the Snake Animation Work?**  

1. Create a new branch named **"output"** in your GitHub profile repository.  
2. Go to **Actions** in your GitHub repo and enable **Workflows**.  
3. Add this YAML file inside **.github/workflows/cobra.yml**:  

```yaml
name: Generate Snake Animation

on:
  schedule:
    - cron: "0 0 * * *"  # Runs daily at midnight UTC
  workflow_dispatch:

jobs:
  generate:
    runs-on: ubuntu-latest
    steps:
      - name: Checkout repository
        uses: actions/checkout@v3

      - name: Generate the snake animation
        uses: Platane/snk@master
        with:
          github_user_name: ${{ github.repository_owner }}
          outputs: |
            github-snake.svg
            github-snake-dark.svg?palette=github-dark

      - name: Push generated files
        uses: actions/upload-artifact@v3
        with:
          name: Snake Animation
          path: |
            github-snake.svg
            github-snake-dark.svg?palette=github-dark
