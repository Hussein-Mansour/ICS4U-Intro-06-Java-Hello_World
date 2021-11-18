.github/workflows/main.yml

###############################################
# Run GitHub's Super Linter against code base #
###############################################

name: GitHub's Super Linter

on: [push, pull_request]

jobs:
  run-linters:
    name: GitHub's Super Linter
    runs-on: ubuntu-latest

    steps:
      - name: Check out Git repository
        uses: actions/checkout@master
        
      - name: Run GitHub Super Linter
        uses: github/super-linter@main
        env:
          VALIDATE_ALL_CODEBASE: true
          VALIDATE_JAVASCRIPT_STANDARD: false
          VALIDATE_CLANG_FORMAT: false
          DEFAULT_BRANCH: main
          GITHUB_TOKEN: ${{ secrets.GITHUB_TOKEN }}
          
          
          
[![GitHub's Super Linter](https://github.com/Hussein-Mansour/ICS4U-Intro-06-Java-Hello_World/workflows/GitHub's%20Super%20Linter/badge.svg)](https://github.com/Hussein-Mansour/ICS4U-Intro-06-Java-Hello_World/actions)        
