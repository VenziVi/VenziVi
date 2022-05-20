
[![Top Langs](https://github-readme-stats.vercel.app/api/top-langs/?username=VenziVi&layout=compact)](https://github.com/VenziVi/github-readme-stats)

name: Waka Readme

on:
  schedule:
    # Runs at 12am IST
    - cron: '30 18 * * *'
  workflow_dispatch:
jobs:
  update-readme:
    name: Update Readme with Metrics
    runs-on: windows
    steps:
      - uses: VenziVi/waka-readme-stats@VenziVi
        with:
          WAKATIME_API_KEY: ${{ secrets.WAKATIME_API_KEY }}
          GH_TOKEN: ${{ secrets.GH_TOKEN }}
