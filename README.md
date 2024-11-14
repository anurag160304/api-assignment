# api-assignment
This is my first repository . In this repo i push my api assignment of coding ninja ml course.
import requests 
import json
import pandas as pd

headers = {
    "Authorization": "Bearer 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",
    "X-GitHub-Api-Version": "2022-11-28"
}

response = requests.get("https://api.github.com/orgs/CodingNinjasCodes/repos", headers=headers)
repositories=response.json()
for repo in repositories:
    name = repo['name']
    forks_count = repo['forks_count']
    watchers_count = repo['watchers_count']
    print(f"Repository_name= {name} ,forkscount = {forks_count} ,watcherscount = {watchers_count}")
