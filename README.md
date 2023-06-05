## Environment

To build the bot using this source-code, setup all vars manually and fill it at eduu/config.py file.

### Deploy on Heroku (PAID)
1. Fork this repo
2. Visit heroku.com
3. Create new App -> Enter the App Name -> Choose App Country
4. Click on Deploy Tab
5. Click on GitHub Tab -> Connect the App to Your GitHub account
6. Enter the Repo name You've forked before -> Tap Connect
7. Click on Deploy Branch button
8. After build done -> Click on Resources Tab -> Switch Toggle On

### Deploy on VPS/LINUX/HEROKU

<p align="center"><a href="https://dashboard.heroku.com/new?template=https://github.com/TOXIC-BOY-OP/GUARD-ROBOT"> <img src="https://img.shields.io/badge/Deploy%20On%20Heroku-yellow?style=for-the-badge&logo=heroku" width="420" height="38.45"/></a></p>

Clone the repo first
```bash
git clone https://github.com/TOXIC-BOY-OP/GUARD-ROBOT
```

```bash
# install python3-venv
sudo apt install python3-venv
# activate venv
python3 -m venv venv
. ./venv/bin/activate
# install requirements
pip install -Ur requirements.txt
# setup config
cd eduu
nano config.py (type CTRL + s to save change & CTRL + x to exit)
cd .. (exit from eduu directory)
# run the bot
python3 -m eduu
```

Or if you using systemd take a look at [this](https://gist.github.com/Zxce3/584309dade0a72e4eb8423f6fc44e594)

make a file named `eduubot.service` and fill it with one of there

```ini
[Unit]
Description=EduuBot
After=network.target

[Service]
Type=simple
User=youruser
WorkingDirectory=/path/to/eduubot
# if you using venv
ExecStart=/path/to/venv/bin/python3 -m eduu
# if you not using venv
# ExecStart=/usr/bin/python3 -m eduu
Restart=always

[Install]
WantedBy=multi-user.target
```

Then run this command

```bash
sudo cp eduubot.service /etc/systemd/system/
sudo systemctl daemon-reload
sudo systemctl enable eduubot
sudo systemctl start eduubot
```

## Credit

This source-code is fully based on [ToxicTeam's](https://github.com/TOXIC-BOY-OP/GUARD-ROBOT) repo and fully re-edited by me for personal use, and for another else want to use this source-code so thanks to them.

Thanks to [TOXIC](https://github.com/TOXIC-BOY-OP) for his Contribution on making clone feature.
