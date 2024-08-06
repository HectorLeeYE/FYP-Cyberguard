# CyberGuard SMU 

Date Ported Over: 060824


# Suggestions
1. I suggest creating a virtual environment before you install anything. It's gonna get BIGGGG

# IMPORTANT
Since its all local containers, dont forget to build with `cyberguard_fastapi:latest` tag, so its `docker build -t cyberguard_fastapi:latest .` **before** you do `docker-compose up -d`


# Commands
1. `docker plugin install grafana/loki-docker-driver:latest --alias loki --grant-all-permissions`
2. `docker-compose up -d`
3. `docker plugin enable loki`              **Use this if your step 2 throws an error**
4. `pip install locust`
5. `locust -f locustfile.py --headless --users 10 --spawn-rate 1 -H http://localhost:8000`
6. `pip install -r requirements.txt`

# Instructions
1. Once you're done with the installation, just open up http://localhost:3000
2. The login instructions are admin:admin 