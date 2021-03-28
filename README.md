- 👋 Hi, I’m @Santhoshstark06
- 👀 I’m interested in coding.
- 🌱 I’m currently learning python.
- 💞️ I’m looking to collaborate on python projects.
- 📫 How to reach me by asanthoshkumar01@gmail.com

name: GitHub - Activity - Readme

on:
  schedule:
    - cron: "0 * * * *"
  workflow_dispatch:

jobs:
  build:
    runs-on: ubuntu-latest

    steps:
      - uses: actions/checkout@v2
      - uses: jamesgeorge007/github-activity-readme@master
        env:
          GITHUB_TOKEN: ${{ secrets.GITHUB_TOKEN }}
          
          name: Latest blog post workflow
on:
  schedule:
    # Runs every hour
    - cron: '0 * * * *'
  workflow_dispatch:

jobs:
  update-readme-with-blog:
    name: Update this repo's README with latest blog posts
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v2
      - uses: gautamkrishnar/blog-post-workflow@master
        with:
          feed_list: "https://dev.to/feed/codestackr"

