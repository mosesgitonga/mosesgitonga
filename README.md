# 💫 About Me:
Am currently an ALX AFRICA Software engineering student.<br>Ask me anything about c, Python and linux Shell scripting.<br>Am open to opportunities in the computer science field.


# 💻 Tech Stack:
![C](https://img.shields.io/badge/c-%2300599C.svg?style=for-the-badge&logo=c&logoColor=white) ![CSS3](https://img.shields.io/badge/css3-%231572B6.svg?style=for-the-badge&logo=css3&logoColor=white) ![HTML5](https://img.shields.io/badge/html5-%23E34F26.svg?style=for-the-badge&logo=html5&logoColor=white) ![Python](https://img.shields.io/badge/python-3670A0?style=for-the-badge&logo=python&logoColor=ffdd54) ![Shell Script](https://img.shields.io/badge/shell_script-%23121011.svg?style=for-the-badge&logo=gnu-bash&logoColor=white) ![LINUX](https://img.shields.io/badge/Linux-FCC624?style=for-the-badge&logo=linux&logoColor=black)
# 📊 GitHub Stats:
![](https://github-readme-stats.vercel.app/api?username=mosesgitonga&theme=dark&hide_border=false&include_all_commits=true&count_private=true)<br/>
![](https://github-readme-streak-stats.herokuapp.com/?user=mosesgitonga&theme=dark&hide_border=false)<br/>
![](https://github-readme-stats.vercel.app/api/top-langs/?username=mosesgitonga&theme=dark&hide_border=false&include_all_commits=true&count_private=true&layout=compact)

## 🏆 GitHub Trophies
![](https://github-profile-trophy.vercel.app/?username=mosesgitonga&theme=radical&no-frame=false&no-bg=true&margin-w=4)

### ✍️ Random Dev Quote
![](https://quotes-github-readme.vercel.app/api?type=horizontal&theme=radical)

### 🔝 Top Contributed Repo
![](https://github-contributor-stats.vercel.app/api?username=mosesgitonga&limit=5&theme=dark&combine_all_yearly_contributions=true)

### 😂 Random Dev Meme
<img src="https://rm.up.railway.app/" width="512px"/>
<a href="https://visitcount.itsvg.in">
  <img src="https://visitcount.itsvg.in/api?id=mosesgitonga&label=Profile%20Views&icon=5&pretty=false" />
</a>


---
[![](https://visitcount.itsvg.in/api?id=mosesgitonga&icon=0&color=0)](https://visitcount.itsvg.in)

import requests

def get_visitors(username):
    url = "https://api.github.com/users/{}/received_events".format(username)
    response = requests.get(url)
    if response.status_code == 200:
        events = response.json()
        visitors = []
        for event in events:
            if event["type"] == "WatchEvent":
                visitors.append(event["actor"]["login"])
        return visitors
    else:
        print("Error: {} {}".format(response.status_code, response.reason))

if __name__ == "__main__":
    username = input("Enter your GitHub username: ")
    visitors = get_visitors(username)
    print("The following people have visited your GitHub profile:")
    for visitor in visitors:
        print(visitor)

<!-- Proudly created with GPRM ( https://gprm.itsvg.in ) -->
