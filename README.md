# V2RayAggregator


[![Collect](https://github.com/mahdibland/SSAggregator/actions/workflows/Collector.yml/badge.svg)](https://github.com/mahdibland/SSAggregator/actions/workflows/Collector.yml) [![Airport Collect](https://github.com/mahdibland/SSAggregator/actions/workflows/Airport_Collector.yml/badge.svg)](https://github.com/mahdibland/SSAggregator/actions/workflows/Airport_Collector.yml)

## Quick Note & Updates
🔴 ~~This project is still under maintance. so don't use it until further announcement cause there is a chance you will get errors while updating the nodes, etc.~~  

🟢 11/1/2022: from now you can use this project. also readme file updated with the recent changes so you can find out which file to use.

## Introduction

The automation functions of this repository are all implemented based on `GitHub Actions`

Test the speed of each free node pool on the network and the nodes shared by bloggers to screen out relatively stable and high-speed nodes, and then import them into the warehouse for sharing records.

The speed measurement function is implemented in the `GitHub Actions` environment using [LiteSpeedTest](https://github.com/xxf098/LiteSpeedTest), so there are many nodes in the United States, which cannot well represent the node availability in the domestic network environment.

## Features
- Lots of sources 😯
- Remove all duplicate nodes 🤤
- Providing nodes in major formats (YAML, clash, v2ray, base64) 🦋
- No additional conversion to prevent breaking the nodes 🌿
- Filtering best nodes by testing them and sorting them based on their average speed 🍀

## Recent Todos
- [x] ~~Fix region based lite speed test (mainly EU)~~ 👀
- [x] Fix Sort Based on the Avg Speed 👀
- [x] Update required softwares to latest version 👀
- [x] Fix sources that subconvertor unable to convert 👀
- [x] Add separate files & functions for airport 👀
- [x] Fix name (emoji+ip) for all log files 👀
- [x] Separate sub list for airports & other nodes 👀
- [x] Fixed clash template 👀
- [ ] Cleanup redundant files and functions (dev Branch) 🧲

## Visualizer

- Log Visualizer on Netlify 
> if you click on any node url it will copy to clipboard



|                  |             Link to Log              |
|:----------------:|:-----------------------------:|
|   Public Nodes   |   <a href="https://55292969231427515295.netlify.app/" target="_blank"><img src="https://i.ibb.co/g32RmJy/netlify.png" width="35"/></a>   |
|     Airport      |   <a href="https://55292969231427515295.netlify.app?type=airport" target="_blank"><img src="https://i.ibb.co/g32RmJy/netlify.png" width="35"/></a>   |

## Instructions & Usage

### Tips
- If you see an IP repeated more than once it's usually because of the different ports.
- (Group 2) Some free airports only provide 1GB of traffic or have limited time to use that's why I update the airport node every 2 hours. so if you want to use them set the auto-update option on your client to get fresh nodes.
- (Group 1) Other public nodes are more stable and will be updated every 12 hours.
- Depending on your internet provider and location, some nodes might not work.


### Ready to import (200 filtered nodes)
> Just import the following subscription link into the corresponding client. Use a client that atleast support ss + ssr + vmess + trojan.

Nodes filtered using speedtest measurement will be stored in following files:  

* Group 1 (Contains free public nodes)
- [Base64](https://raw.githubusercontent.com/mahdibland/ShadowsocksAggregator/master/Eternity)
- [Mixed](https://raw.githubusercontent.com/mahdibland/ShadowsocksAggregator/master/Eternity.txt)
- [Clash](https://raw.githubusercontent.com/mahdibland/ShadowsocksAggregator/master/Eternity.yml)

* Group 2 (Contains only free airports)
- [Base64](https://raw.githubusercontent.com/mahdibland/ShadowsocksAggregator/master/EternityAir)
- [Mixed](https://raw.githubusercontent.com/mahdibland/ShadowsocksAggregator/master/EternityAir.txt)
- [Clash](https://raw.githubusercontent.com/mahdibland/ShadowsocksAggregator/master/EternityAir.yml)

### For Local Testing (all nodes)
> Only for local testing because the number of nodes is too high and your client will crash if you import them  

All of the nodes merged together will be stored in following files:  

* Group 1 (Contains free public nodes)
- [Base64](https://raw.githubusercontent.com/mahdibland/SSAggregator/master/sub/sub_merge_base64.txt)
- [Mixed](https://raw.githubusercontent.com/mahdibland/SSAggregator/master/sub/sub_merge.txt)
- [Clash](https://raw.githubusercontent.com/mahdibland/SSAggregator/master/sub/sub_merge_yaml.yml)

* Group 2 (Contains only free airports)
- [Base64](https://raw.githubusercontent.com/mahdibland/SSAggregator/master/sub/airport_merge_base64.txt)
- [Mixed](https://raw.githubusercontent.com/mahdibland/SSAggregator/master/sub/airport_sub_merge.txt)
- [Clash](https://raw.githubusercontent.com/mahdibland/SSAggregator/master/sub/airport_merge_yaml.yml)

### Manual Subs Conversion
- If your client does not support the formats that provided here use below services to convert them to your client format (like surfboard)
> Services for online sub conversion: 
- [sub-web-modify](https://sub.v1.mk/)
- [bianyuan](https://bianyuan.xyz/)  

- **If you don't like the groups and rules that are already set, you can simply use bianyuan API like this::**  
> don't use this API for your personal airport subs! Pls run the subconverter locally
```
https://pub-api-1.bianyuan.xyz/sub?target=(OutputFormat)&url=(SubUrl)&insert=false

For Example:
(OutputFormat) = clash
(SubUrl) = https://raw.githubusercontent.com/mahdibland/ShadowsocksAggregator/master/Eternity.yml

https://pub-api-1.bianyuan.xyz/sub?target=clash&url=https://raw.githubusercontent.com/mahdibland/ShadowsocksAggregator/master/Eternity.yml&insert=false

Now you can use the link above to import the subs into your client
```

<br/>

## Node Information

### high-speed node
high-speed node quantity: `200`

<details>
    trojan://dfbf0d67-f03d-4184-a224-c2d64a571f99@s1.hass.win:12340?allowInsecure=1&sni=static.dingtalk.com#%F0%9F%87%BA%F0%9F%87%B8US-147.182.224.102-12778
    vmess://ewogICAgImFkZCI6ICJjbG91ZGdldHNlcnZpY2UubWNsb3Vkc2VydmljZS5zaXRlIiwKICAgICJhaWQiOiAwLAogICAgImhvc3QiOiAiVXNhLVZwLTE5Mi5ibGF6RWNsb3VkTUFpbi5TaXRFIiwKICAgICJpZCI6ICI5NmU0NGEyMi00ZjVjLTQ4ZjktOTlkOS1mMmMxOTg1ZGQ1YjkiLAogICAgIm5ldCI6ICJ3cyIsCiAgICAicGF0aCI6ICIvbGlua3Zrd3MiLAogICAgInBvcnQiOiA0NDMsCiAgICAicHMiOiAi8J+PgVJFTEFZLTE3Mi42Ni4xNjguMjA5LTY1NCIsCiAgICAidGxzIjogInRscyIsCiAgICAidHlwZSI6ICJhdXRvIiwKICAgICJzZWN1cml0eSI6ICJhdXRvIiwKICAgICJza2lwLWNlcnQtdmVyaWZ5IjogdHJ1ZSwKICAgICJzbmkiOiAiIgp9
    ss://Y2hhY2hhMjAtaWV0Zi1wb2x5MTMwNTpmOWQ3M2M4NGUzMmExMGYz@57.128.190.171:11259#%F0%9F%87%AB%F0%9F%87%B7FR-57.128.190.171-167
    ss://YWVzLTI1Ni1nY206STFoVG1hMEJvTA==@uk.ir.iranigamepars.ir:443#%F0%9F%87%AC%F0%9F%87%A7GB-92.119.199.33-665
    vmess://ewogICAgImFkZCI6ICJ3d3cuaGRtb2xpLmNvbSIsCiAgICAiYWlkIjogMCwKICAgICJob3N0IjogImZyLmZyZWV5eWRzLmRwZG5zLm9yZyIsCiAgICAiaWQiOiAiMmYzOGY4NDgtYTg5OS00Yzg3LTk4MDctMjA3YTQxNjE1ZTNjIiwKICAgICJuZXQiOiAid3MiLAogICAgInBhdGgiOiAiL3JvbmdzZXZlbj9lZD0yMDQ4IiwKICAgICJwb3J0IjogODAsCiAgICAicHMiOiAi8J+PgVJFTEFZLTEwNC4yMS43Mi4yMzMtMDE2IiwKICAgICJ0bHMiOiAiIiwKICAgICJ0eXBlIjogImF1dG8iLAogICAgInNlY3VyaXR5IjogImF1dG8iLAogICAgInNraXAtY2VydC12ZXJpZnkiOiB0cnVlLAogICAgInNuaSI6ICIiCn0=
    ss://Y2hhY2hhMjAtaWV0Zi1wb2x5MTMwNTpYaHJteUtFNkY5QlFDaW9naWdKMUlE@77.110.106.74:31465#%F0%9F%87%AB%F0%9F%87%B7FR-77.110.106.74-161
    ss://Y2hhY2hhMjAtaWV0Zi1wb2x5MTMwNTo2N2RZZmkxdUF2MlpUeFh2TG9lazM5@66.151.41.89:33133#%F0%9F%87%A9%F0%9F%87%AADE-66.151.41.89-008
    ss://Y2hhY2hhMjAtaWV0Zi1wb2x5MTMwNToxQVU2Tmd1cG9scU5kU0owRHgxbms3@185.42.163.45:25108#%F0%9F%87%AB%F0%9F%87%AEFI-185.42.163.45-648
    ss://YWVzLTI1Ni1jZmI6YXdzcHMwNTAx@43.206.214.213:443#%F0%9F%87%AF%F0%9F%87%B5JP-43.206.214.213-689
    ss://YWVzLTI1Ni1jZmI6YXdzcHMwNTAx@18.179.178.170:443#%F0%9F%87%AF%F0%9F%87%B5JP-18.179.178.170-674
    trojan://telegram-id-privatevpns@63.176.54.26:22222?security=tls&sni=trojan.burgerip.co.uk#%F0%9F%87%A9%F0%9F%87%AADE-63.176.54.26-651
    ss://Y2hhY2hhMjAtaWV0Zi1wb2x5MTMwNTpCZ3I2WUJIRW5wZnQ=@178.22.31.239:443#%F0%9F%87%A6%F0%9F%87%B9AT-178.22.31.239-166
    ss://Y2hhY2hhMjAtaWV0Zi1wb2x5MTMwNTo5b25GRVdwUmdLbXRNbnh0WEdJV0Qw@77.110.102.235:64864#%F0%9F%87%B3%F0%9F%87%B1NL-77.110.102.235-162
    ss://YWVzLTI1Ni1jZmI6WG44aktkbURNMDBJZU8lIyQjZkpBTXRzRUFFVU9wSC9ZV1l0WXFERm5UMFNW@103.186.154.30:38388#%F0%9F%87%BB%F0%9F%87%B3VN-103.186.154.30-670
    trojan://telegram-id-directvpn@63.176.54.26:22223?security=tls&sni=trojan.burgerip.co.uk#%F0%9F%87%A9%F0%9F%87%AADE-63.176.54.26-003
    vmess://ewogICAgImFkZCI6ICIxMDQuMTguMTQ5Ljc2IiwKICAgICJhaWQiOiAwLAogICAgImhvc3QiOiAidXMua2twLm1lLmV1Lm9yZyIsCiAgICAiaWQiOiAiZGU5NGNjMGEtMDU5Mi00OTY5LWIxZmMtOTdlYThmMGVhMGIzIiwKICAgICJuZXQiOiAid3MiLAogICAgInBhdGgiOiAiL2FhIiwKICAgICJwb3J0IjogNDQzLAogICAgInBzIjogIvCfj4FSRUxBWS0xMDQuMTguMTQ5Ljc2LTAyMSIsCiAgICAidGxzIjogInRscyIsCiAgICAidHlwZSI6ICJhdXRvIiwKICAgICJzZWN1cml0eSI6ICJhdXRvIiwKICAgICJza2lwLWNlcnQtdmVyaWZ5IjogZmFsc2UsCiAgICAic25pIjogInVzLmtrcC5tZS5ldS5vcmciCn0=
    ss://Y2hhY2hhMjAtaWV0Zi1wb2x5MTMwNTpvWEdwMStpaGxmS2c4MjZI@204.136.10.115:1866#%F0%9F%87%A8%F0%9F%87%ADCH-204.136.10.115-163
    vmess://ewogICAgImFkZCI6ICI1MS43OS4xMDIuMjUzIiwKICAgICJhaWQiOiAwLAogICAgImhvc3QiOiAiNTEuNzkuMTAyLjI1MyIsCiAgICAiaWQiOiAiNThmZTE1NDItNTI5MC00MGFkLTgxNWEtNzc3MDdhODFhZmU1IiwKICAgICJuZXQiOiAid3MiLAogICAgInBhdGgiOiAiL0lPZWJoTE1obDFDVGJGSGJMOTVteWZSWDIiLAogICAgInBvcnQiOiA4MCwKICAgICJwcyI6ICLwn4eo8J+HpkNBLTUxLjc5LjEwMi4yNTMtMTYwIiwKICAgICJ0bHMiOiAiIiwKICAgICJ0eXBlIjogImF1dG8iLAogICAgInNlY3VyaXR5IjogImF1dG8iLAogICAgInNraXAtY2VydC12ZXJpZnkiOiB0cnVlLAogICAgInNuaSI6ICIiCn0=
    vmess://ewogICAgImFkZCI6ICI0M2I1YTYxNi1zdzA0ZzAtc3dhc3YzLWx1d2UuaGdjMS50Y3BiYnIubmV0IiwKICAgICJhaWQiOiAwLAogICAgImhvc3QiOiAiYnJvYWRjYXN0bHYuY2hhdC5iaWxpYmlsaS5jb20iLAogICAgImlkIjogImEyYjBmZDJiLTcxNmYtMGRmOC1kNGUyLTAzYTFjMDBlNWYxYSIsCiAgICAibmV0IjogIndzIiwKICAgICJwYXRoIjogIi8iLAogICAgInBvcnQiOiA4MDgwLAogICAgInBzIjogIvCfh63wn4ewSEstMS4zNi4yMjMuMjMzLTY3NyIsCiAgICAidGxzIjogIiIsCiAgICAidHlwZSI6ICJhdXRvIiwKICAgICJzZWN1cml0eSI6ICJhdXRvIiwKICAgICJza2lwLWNlcnQtdmVyaWZ5IjogdHJ1ZSwKICAgICJzbmkiOiAiIgp9
    vmess://ewogICAgImFkZCI6ICIyZTIxY2VEQy1mYThCLTQwMjAtOENlMC0zOTBlNzI4N2QyNzYuODkwNjAzLnBwLlVhIiwKICAgICJhaWQiOiAwLAogICAgImhvc3QiOiAiMmUyMWNlREMtZmE4Qi00MDIwLThDZTAtMzkwZTcyODdkMjc2Ljg5MDYwMy5wcC5VYSIsCiAgICAiaWQiOiAiNTQ1M2FlMjYtMjUwZC00ZTc5LWI0ZWMtMDE2YmFmODA2ODY1IiwKICAgICJuZXQiOiAid3MiLAogICAgInBhdGgiOiAiL2g3UmN1MHkzMGxoamRWakozZ2M0YWoiLAogICAgInBvcnQiOiA0NDMsCiAgICAicHMiOiAi8J+PgVJFTEFZLTEwNC4yMS43MS4yMDUtMTQ4IiwKICAgICJ0bHMiOiAidGxzIiwKICAgICJ0eXBlIjogImF1dG8iLAogICAgInNlY3VyaXR5IjogImF1dG8iLAogICAgInNraXAtY2VydC12ZXJpZnkiOiB0cnVlLAogICAgInNuaSI6ICIiCn0=
    vmess://ewogICAgImFkZCI6ICI1MS43OS4xMDMuNzYiLAogICAgImFpZCI6IDAsCiAgICAiaG9zdCI6ICJ3cm1lbG13eGxmLmdrdGV2bHJxem53cXFvenkuZmFicGZzNjZnaXptbm9qaGN2cXh3bC5reXRyY2Z6cWxhODdndmd2czZjN2tqbnJ1YnVoLmNjIiwKICAgICJpZCI6ICI1OGZlMTU0Mi01MjkwLTQwYWQtODE1YS03NzcwN2E4MWFmZTUiLAogICAgIm5ldCI6ICJ3cyIsCiAgICAicGF0aCI6ICIvSU9lYmhMTWhsMUNUYkZIYkw5NW15ZlJYMiIsCiAgICAicG9ydCI6IDgwLAogICAgInBzIjogIvCfh6jwn4emQ0EtNTEuNzkuMTAzLjc2LTE2NCIsCiAgICAidGxzIjogIiIsCiAgICAidHlwZSI6ICJhdXRvIiwKICAgICJzZWN1cml0eSI6ICJhdXRvIiwKICAgICJza2lwLWNlcnQtdmVyaWZ5IjogdHJ1ZSwKICAgICJzbmkiOiAiIgp9
    trojan://6e1b9a65-884f-3aa9-9469-bf6ec0f08610@sg.singaporenodeserverone.co.ua:443?security=tls&sni=45.32.28.232#%F0%9F%87%B8%F0%9F%87%ACSG-27.122.59.45-669
    ss://Y2hhY2hhMjAtaWV0Zi1wb2x5MTMwNTpWcEtBQmNPcE5OQTBsNUcyQVZPbXc4@213.109.147.242:62685#%F0%9F%87%B3%F0%9F%87%B1NL-213.109.147.242-165
    trojan://3482c71a-d01c-4ae5-b454-fa8cb3785f66@94.131.20.3:443?security=tls&sni=chop-wrist-bud.stark-industries.solutions#%F0%9F%87%BA%F0%9F%87%B8US-94.131.20.3-005
    vmess://ewogICAgImFkZCI6ICJ3d3cueGluanVjLmNvbSIsCiAgICAiYWlkIjogMCwKICAgICJob3N0IjogImhrLmZyZWV5eWRzLmRwZG5zLm9yZyIsCiAgICAiaWQiOiAiMmYzOGY4NDgtYTg5OS00Yzg3LTk4MDctMjA3YTQxNjE1ZTNjIiwKICAgICJuZXQiOiAid3MiLAogICAgInBhdGgiOiAiL3JvbmdzZXZlbj9lZD0yMDQ4IiwKICAgICJwb3J0IjogODAsCiAgICAicHMiOiAi8J+PgVJFTEFZLTE3Mi42Ny4xNTguNzEtMDE3IiwKICAgICJ0bHMiOiAiIiwKICAgICJ0eXBlIjogImF1dG8iLAogICAgInNlY3VyaXR5IjogImF1dG8iLAogICAgInNraXAtY2VydC12ZXJpZnkiOiB0cnVlLAogICAgInNuaSI6ICIiCn0=
    vmess://ewogICAgImFkZCI6ICIyZTIxY2VkYy1mYThiLTQwMjAtOGNlMC0zOTBlNzI4N2QyNzYuODkwNjAzLnBwLnVhIiwKICAgICJhaWQiOiAwLAogICAgImhvc3QiOiAiMkUyMUNFRGMtZkE4Qi00MDIwLThDZTAtMzkwZTcyODdEMjc2Ljg5MDYwMy5QcC51QSIsCiAgICAiaWQiOiAiNTQ1M2FlMjYtMjUwZC00ZTc5LWI0ZWMtMDE2YmFmODA2ODY1IiwKICAgICJuZXQiOiAid3MiLAogICAgInBhdGgiOiAiL2g3UmN1MHkzMGxoamRWakozZ2M0YWoiLAogICAgInBvcnQiOiA0NDMsCiAgICAicHMiOiAi8J+PgVJFTEFZLTE3Mi42Ny4xNDkuNDMtMDQ4IiwKICAgICJ0bHMiOiAidGxzIiwKICAgICJ0eXBlIjogImF1dG8iLAogICAgInNlY3VyaXR5IjogImF1dG8iLAogICAgInNraXAtY2VydC12ZXJpZnkiOiB0cnVlLAogICAgInNuaSI6ICIiCn0=
    ss://Y2hhY2hhMjAtaWV0Zi1wb2x5MTMwNTpvWEdwMStpaGxmS2c4MjZI@185.177.229.245:1866#%F0%9F%87%A9%F0%9F%87%AADE-185.177.229.245-168
    ss://YWVzLTI1Ni1jZmI6WG44aktkbURNMDBJZU8lIyQjZkpBTXRzRUFFVU9wSC9ZV1l0WXFERm5UMFNW@103.186.155.19:38388#%F0%9F%87%BB%F0%9F%87%B3VN-103.186.155.19-492
    vmess://ewogICAgImFkZCI6ICJkZTAxLnNoLWNsb3VkZmxhcmUuc2JzIiwKICAgICJhaWQiOiAwLAogICAgImhvc3QiOiAiZGUwMS5zaC1jbG91ZGZsYXJlLnNicyIsCiAgICAiaWQiOiAiYjM5MjhmOGQtZWE4MS00ZDc1LWJjZWMtNDAxNmEwNzJhZGZmIiwKICAgICJuZXQiOiAid3MiLAogICAgInBhdGgiOiAiLyIsCiAgICAicG9ydCI6IDIwOTYsCiAgICAicHMiOiAi8J+PgVJFTEFZLTEwNC4yMS4xNi4xLTA0MSIsCiAgICAidGxzIjogInRscyIsCiAgICAidHlwZSI6ICJhdXRvIiwKICAgICJzZWN1cml0eSI6ICJhdXRvIiwKICAgICJza2lwLWNlcnQtdmVyaWZ5IjogZmFsc2UsCiAgICAic25pIjogImRlMDEuc2gtY2xvdWRmbGFyZS5zYnMiCn0=
    vmess://ewogICAgImFkZCI6ICIxNDQuMjQuMjAwLjE2NCIsCiAgICAiYWlkIjogMCwKICAgICJob3N0IjogImJleW9uZGRzei5jZmQiLAogICAgImlkIjogIjliNDU2YzJhLWYyYzEtNDVlMS04N2E5LWI3NjI4YjA0YmIyNCIsCiAgICAibmV0IjogIndzIiwKICAgICJwYXRoIjogIi9saW5rd3MiLAogICAgInBvcnQiOiA0NDMsCiAgICAicHMiOiAi8J+Hq/Cfh7dGUi0xNDQuMjQuMjAwLjE2NC02NTAiLAogICAgInRscyI6ICJ0bHMiLAogICAgInR5cGUiOiAiYXV0byIsCiAgICAic2VjdXJpdHkiOiAiYXV0byIsCiAgICAic2tpcC1jZXJ0LXZlcmlmeSI6IHRydWUsCiAgICAic25pIjogIiIKfQ==
    ss://YWVzLTI1Ni1jZmI6WG44aktkbURNMDBJZU8lIyQjZkpBTXRzRUFFVU9wSC9ZV1l0WXFERm5UMFNW@103.186.155.19:38388#%F0%9F%87%BB%F0%9F%87%B3VN-103.186.155.19-133
    ss://YWVzLTI1Ni1nY206Y2RCSURWNDJEQ3duZklO@38.114.114.108:8119#%F0%9F%87%BA%F0%9F%87%B8US-38.114.114.108-687
    vmess://ewogICAgImFkZCI6ICIxMDQuMjEuNjQuMSIsCiAgICAiYWlkIjogMCwKICAgICJob3N0IjogInJhazIuODkwNjAzLnh5eiIsCiAgICAiaWQiOiAiMDI0NWMyZDQtMGFkMS00ZjBmLWViOWMtZmJkNWYxYzQ3YmU3IiwKICAgICJuZXQiOiAid3MiLAogICAgInBhdGgiOiAiLyIsCiAgICAicG9ydCI6IDIwODcsCiAgICAicHMiOiAi8J+PgVJFTEFZLTEwNC4yMS42NC4xLTE0MCIsCiAgICAidGxzIjogInRscyIsCiAgICAidHlwZSI6ICJhdXRvIiwKICAgICJzZWN1cml0eSI6ICJhdXRvIiwKICAgICJza2lwLWNlcnQtdmVyaWZ5IjogdHJ1ZSwKICAgICJzbmkiOiAiIgp9
    ss://YWVzLTI1Ni1jZmI6ZjhmN2FDemNQS2JzRjhwMw==@185.231.233.112:989#%F0%9F%87%B5%F0%9F%87%B9PT-185.231.233.112-006
    ss://Y2hhY2hhMjAtaWV0Zi1wb2x5MTMwNTowUnNyY0ZKMXZPc1dFcWczUDU1aHZhYWNLZnVTaFQwY2MxaDB0OEFEME5BOHUxdVI=@92.38.171.215:31348#%F0%9F%87%AA%F0%9F%87%B8ES-92.38.171.215-004
    ss://Y2hhY2hhMjAtaWV0Zi1wb2x5MTMwNTphNDRlNjc4ZC01NDNlLTQ5ZTItOGNiNy0zOTk5ZTRmY2U1OTI=@free.2apzhfa.xyz:31471#%F0%9F%87%A8%F0%9F%87%B3CN-120.232.218.106-077
    ss://Y2hhY2hhMjAtaWV0Zi1wb2x5MTMwNTphNDRlNjc4ZC01NDNlLTQ5ZTItOGNiNy0zOTk5ZTRmY2U1OTI=@free.2apzhfa.xyz:31241#%F0%9F%87%A8%F0%9F%87%B3CN-120.232.218.106-055
    vmess://ewogICAgImFkZCI6ICJmcmVleXguY2xvdWRmbGFyZTg4LmV1Lm9yZyIsCiAgICAiYWlkIjogMCwKICAgICJob3N0IjogImdvLmRhbHVxdWFuLnRvcCIsCiAgICAiaWQiOiAiNTZiOTE1YzAtYmRmOC00NzQ5LWFiNTUtYjQ0ZDA0NjllNDZkIiwKICAgICJuZXQiOiAid3MiLAogICAgInBhdGgiOiAiLyIsCiAgICAicG9ydCI6IDQ0MywKICAgICJwcyI6ICLwn4+BUkVMQVktMTQxLjEwMS4xMjEuMjIwLTAzOSIsCiAgICAidGxzIjogIiIsCiAgICAidHlwZSI6ICJhdXRvIiwKICAgICJzZWN1cml0eSI6ICJhdXRvIiwKICAgICJza2lwLWNlcnQtdmVyaWZ5IjogdHJ1ZSwKICAgICJzbmkiOiAiIgp9
    vmess://ewogICAgImFkZCI6ICJwaHgtcGx1cy0xZGRucy5mYWZvcmV4LmV1Lm9yZyIsCiAgICAiYWlkIjogMCwKICAgICJob3N0IjogInBoeC1wbHVzLTFkZG5zLmZhZm9yZXguZXUub3JnIiwKICAgICJpZCI6ICJmODQ1ZmFiYS1lZjA3LTRlZjAtYjA1NS04NjZiYmI4MTE0M2MiLAogICAgIm5ldCI6ICJ3cyIsCiAgICAicGF0aCI6ICIvIiwKICAgICJwb3J0IjogMjM0NTEsCiAgICAicHMiOiAi8J+HuvCfh7hVUy0xNDQuMjQuNC4xMzAtMDQwIiwKICAgICJ0bHMiOiAiIiwKICAgICJ0eXBlIjogImF1dG8iLAogICAgInNlY3VyaXR5IjogImF1dG8iLAogICAgInNraXAtY2VydC12ZXJpZnkiOiB0cnVlLAogICAgInNuaSI6ICIiCn0=
    vmess://ewogICAgImFkZCI6ICIyMTMuMjQxLjE5OC41NyIsCiAgICAiYWlkIjogMCwKICAgICJob3N0IjogImxheDEuaWJnZncudG9wIiwKICAgICJpZCI6ICIxOTFiYWJjNS0yYWFmLTRmZTUtYTU2My1mMTQyNDRhZWZiNGUiLAogICAgIm5ldCI6ICJ3cyIsCiAgICAicGF0aCI6ICIveHJlbnZ3cyIsCiAgICAicG9ydCI6IDg0NDMsCiAgICAicHMiOiAi8J+PgVJFTEFZLTIxMy4yNDEuMTk4LjU3LTAzNyIsCiAgICAidGxzIjogInRscyIsCiAgICAidHlwZSI6ICJhdXRvIiwKICAgICJzZWN1cml0eSI6ICJhdXRvIiwKICAgICJza2lwLWNlcnQtdmVyaWZ5IjogdHJ1ZSwKICAgICJzbmkiOiAiIgp9
    vmess://ewogICAgImFkZCI6ICJmcmFua2Z1cnQuZmFmb3JleC5ldS5vcmciLAogICAgImFpZCI6IDAsCiAgICAiaG9zdCI6ICJ1cy1uZXcwMy5kYWx1cXVhbi50b3AiLAogICAgImlkIjogIjRlMzA5YzE4LWVlNWYtNDVmMy04ZjI4LTY2NDY3ZDFlMGM0ZiIsCiAgICAibmV0IjogIndzIiwKICAgICJwYXRoIjogIi9pdGRvZz9lZD0yNTYwIiwKICAgICJwb3J0IjogMjM0NTEsCiAgICAicHMiOiAi8J+HqfCfh6pERS0xNTguMTgwLjQ4LjE5LTA0MiIsCiAgICAidGxzIjogIiIsCiAgICAidHlwZSI6ICJhdXRvIiwKICAgICJzZWN1cml0eSI6ICJhdXRvIiwKICAgICJza2lwLWNlcnQtdmVyaWZ5IjogdHJ1ZSwKICAgICJzbmkiOiAiIgp9
    vmess://ewogICAgImFkZCI6ICIxNDQuMjIuMjE2LjY4IiwKICAgICJhaWQiOiAwLAogICAgImhvc3QiOiAiYnIzLnZwMTAwMC5uZXQiLAogICAgImlkIjogImE5MzI2YTVhLWI4OTAtNDZlMy1iZDNkLWE0ZjlkNTA4MjMyMyIsCiAgICAibmV0IjogIndzIiwKICAgICJwYXRoIjogIi9wdWxpY3BEaXNuZXkiLAogICAgInBvcnQiOiA4NDQzLAogICAgInBzIjogIvCfh6fwn4e3QlItMTQ0LjIyLjIxNi42OC0wNDMiLAogICAgInRscyI6ICJ0bHMiLAogICAgInR5cGUiOiAiYXV0byIsCiAgICAic2VjdXJpdHkiOiAiYXV0byIsCiAgICAic2tpcC1jZXJ0LXZlcmlmeSI6IHRydWUsCiAgICAic25pIjogIiIKfQ==
    vmess://ewogICAgImFkZCI6ICJ1czE0OC52cDEwMDAubmV0IiwKICAgICJhaWQiOiAwLAogICAgImhvc3QiOiAidXMxNDgudnAxMDAwLm5ldCIsCiAgICAiaWQiOiAiYTkzMjZhNWEtYjg5MC00NmUzLWJkM2QtYTRmOWQ1MDgyMzIzIiwKICAgICJuZXQiOiAid3MiLAogICAgInBhdGgiOiAiL2NwMTAwdnA4MDBra2tkc254IiwKICAgICJwb3J0IjogNDQzLAogICAgInBzIjogIvCfj4FSRUxBWS0xMDQuMjEuMTQuMjM1LTA0NCIsCiAgICAidGxzIjogInRscyIsCiAgICAidHlwZSI6ICJhdXRvIiwKICAgICJzZWN1cml0eSI6ICJhdXRvIiwKICAgICJza2lwLWNlcnQtdmVyaWZ5IjogdHJ1ZSwKICAgICJzbmkiOiAiIgp9
    vmess://ewogICAgImFkZCI6ICJ1czAxLnNoLWNsb3VkZmxhcmUuc2JzIiwKICAgICJhaWQiOiAwLAogICAgImhvc3QiOiAidXMwMS5zaC1jbG91ZGZsYXJlLnNicyIsCiAgICAiaWQiOiAiMmJkMGM5ZDctZjIzOS00MzdlLWExZTEtNmNmODMwYWYyYTFhIiwKICAgICJuZXQiOiAid3MiLAogICAgInBhdGgiOiAiLyIsCiAgICAicG9ydCI6IDg0NDMsCiAgICAicHMiOiAi8J+PgVJFTEFZLTEwNC4yMS4zMi4xLTA0NSIsCiAgICAidGxzIjogInRscyIsCiAgICAidHlwZSI6ICJhdXRvIiwKICAgICJzZWN1cml0eSI6ICJhdXRvIiwKICAgICJza2lwLWNlcnQtdmVyaWZ5IjogZmFsc2UsCiAgICAic25pIjogInVzMDEuc2gtY2xvdWRmbGFyZS5zYnMiCn0=
    vmess://ewogICAgImFkZCI6ICJjZG5qcy5jb20iLAogICAgImFpZCI6IDAsCiAgICAiaG9zdCI6ICJjcmVhdGl2ZXNlcnZpY2VzLm5ldGZsaXguY29tLnd1a29uZy5hc29sb2xlLmJpei5pZCIsCiAgICAiaWQiOiAiZGU5NGNjMGEtMDU5Mi00OTY5LWIxZmMtOTdlYThmMGVhMGIzIiwKICAgICJuZXQiOiAid3MiLAogICAgInBhdGgiOiAiL3VzLmtrcC5tZS5ldS5vcmcvYWEiLAogICAgInBvcnQiOiA0NDMsCiAgICAicHMiOiAi8J+PgVJFTEFZLTEwNC4yNC4xOTcuMjAtMDQ2IiwKICAgICJ0bHMiOiAidGxzIiwKICAgICJ0eXBlIjogImF1dG8iLAogICAgInNlY3VyaXR5IjogImF1dG8iLAogICAgInNraXAtY2VydC12ZXJpZnkiOiB0cnVlLAogICAgInNuaSI6ICIiCn0=
    vmess://ewogICAgImFkZCI6ICJ0aW1lLmlzIiwKICAgICJhaWQiOiAwLAogICAgImhvc3QiOiAic2hzMTExLmtlaml4aWFvcWk2NjYuc3RvcmUiLAogICAgImlkIjogIjc2OTA2MmVmLTNlMDktNGNhYS1hOTUxLTg5MmI2ZjI1Y2Y0YSIsCiAgICAibmV0IjogIndzIiwKICAgICJwYXRoIjogIi8iLAogICAgInBvcnQiOiA0NDMsCiAgICAicHMiOiAi8J+PgVJFTEFZLTEwNC4yNi4xMy41NC0wNDciLAogICAgInRscyI6ICJ0bHMiLAogICAgInR5cGUiOiAiYXV0byIsCiAgICAic2VjdXJpdHkiOiAiYXV0byIsCiAgICAic2tpcC1jZXJ0LXZlcmlmeSI6IHRydWUsCiAgICAic25pIjogIiIKfQ==
    vmess://ewogICAgImFkZCI6ICIxYTJkNTE0Yi0zN2NmLTQ5OWYtOGQwOC1kMDE3YTkyYWI1YmIuYXNvdWwtYXZhLnRvcCIsCiAgICAiYWlkIjogMCwKICAgICJob3N0IjogIjFhMmQ1MTRiLTM3Y2YtNDk5Zi04ZDA4LWQwMTdhOTJhYjViYi5hc291bC1hdmEudG9wIiwKICAgICJpZCI6ICI1ZjcyNmZlMy1kODJlLTRkYTUtYTcxMS04YWYwY2JiMmI2ODIiLAogICAgIm5ldCI6ICJ3cyIsCiAgICAicGF0aCI6ICIvIiwKICAgICJwb3J0IjogNDQzLAogICAgInBzIjogIvCfj4FSRUxBWS0xNzIuNjcuMjAwLjEzLTAzNiIsCiAgICAidGxzIjogInRscyIsCiAgICAidHlwZSI6ICJhdXRvIiwKICAgICJzZWN1cml0eSI6ICJhdXRvIiwKICAgICJza2lwLWNlcnQtdmVyaWZ5IjogZmFsc2UsCiAgICAic25pIjogIjFhMmQ1MTRiLTM3Y2YtNDk5Zi04ZDA4LWQwMTdhOTJhYjViYi5hc291bC1hdmEudG9wIgp9
    trojan://15b24b56-d667-4fa8-b548-f3dc942fb461@104.21.34.159:443?security=tls&sni=2qwert.2031.pp.ua&type=ws&path=/4p35eUnmGxQ8YJFJxz&Host=2qwert.2031.pp.ua#%F0%9F%8F%81RELAY-104.21.34.159-049
    vmess://ewogICAgImFkZCI6ICIxMDQuMTguMTE0LjEiLAogICAgImFpZCI6IDAsCiAgICAiaG9zdCI6ICJtMTE2LjE2NDc0OC54eXoiLAogICAgImlkIjogIjdkOTJmZmM5LTAyZTEtNDA4Ny04YTQ2LWNjNGQ3NjU2MDkxNyIsCiAgICAibmV0IjogIndzIiwKICAgICJwYXRoIjogImdpdGh1Yi5jb20vQWx2aW45OTk5IiwKICAgICJwb3J0IjogMjA4NiwKICAgICJwcyI6ICLwn4+BUkVMQVktMTA0LjE4LjExNC4xLTA1MCIsCiAgICAidGxzIjogIiIsCiAgICAidHlwZSI6ICJhdXRvIiwKICAgICJzZWN1cml0eSI6ICJhdXRvIiwKICAgICJza2lwLWNlcnQtdmVyaWZ5IjogZmFsc2UsCiAgICAic25pIjogIm0xMTYuMTY0NzQ4Lnh5eiIKfQ==
    vmess://ewogICAgImFkZCI6ICIxMDQuMTguMTE0LjIiLAogICAgImFpZCI6IDAsCiAgICAiaG9zdCI6ICJtMTE2LjE2NDc0OC54eXoiLAogICAgImlkIjogIjdkOTJmZmM5LTAyZTEtNDA4Ny04YTQ2LWNjNGQ3NjU2MDkxNyIsCiAgICAibmV0IjogIndzIiwKICAgICJwYXRoIjogImdpdGh1Yi5jb20vQWx2aW45OTk5IiwKICAgICJwb3J0IjogMjA4NiwKICAgICJwcyI6ICLwn4+BUkVMQVktMTA0LjE4LjExNC4yLTA1MSIsCiAgICAidGxzIjogIiIsCiAgICAidHlwZSI6ICJhdXRvIiwKICAgICJzZWN1cml0eSI6ICJhdXRvIiwKICAgICJza2lwLWNlcnQtdmVyaWZ5IjogZmFsc2UsCiAgICAic25pIjogIm0xMTYuMTY0NzQ4Lnh5eiIKfQ==
    ss://Y2hhY2hhMjAtaWV0Zi1wb2x5MTMwNTphNDRlNjc4ZC01NDNlLTQ5ZTItOGNiNy0zOTk5ZTRmY2U1OTI=@free.2apzhfa.xyz:31141#%F0%9F%87%A8%F0%9F%87%B3CN-120.232.218.106-052
    ss://Y2hhY2hhMjAtaWV0Zi1wb2x5MTMwNTphNDRlNjc4ZC01NDNlLTQ5ZTItOGNiNy0zOTk5ZTRmY2U1OTI=@free.2apzhfa.xyz:31143#%F0%9F%87%A8%F0%9F%87%B3CN-120.232.218.106-053
    ss://Y2hhY2hhMjAtaWV0Zi1wb2x5MTMwNTphNDRlNjc4ZC01NDNlLTQ5ZTItOGNiNy0zOTk5ZTRmY2U1OTI=@free.2apzhfa.xyz:31145#%F0%9F%87%A8%F0%9F%87%B3CN-120.232.218.106-054
    vmess://ewogICAgImFkZCI6ICJtcHVzLmNmLmNuYW1lLnZ2aGFuLmNvbSIsCiAgICAiYWlkIjogMCwKICAgICJob3N0IjogInYydXMyLjkwMjIyMi54eXoiLAogICAgImlkIjogImJhY2ZjZGYzLWFiYzEtMzhlZS05YTcwLTZjZmJjNzI2MjFjNyIsCiAgICAibmV0IjogIndzIiwKICAgICJwYXRoIjogIi9obHMvY2N0djVwaGQubTN1OCIsCiAgICAicG9ydCI6IDQ0MywKICAgICJwcyI6ICLwn4+BUkVMQVktMTA0LjE3LjkzLjY2LTE5MCIsCiAgICAidGxzIjogInRscyIsCiAgICAidHlwZSI6ICJhdXRvIiwKICAgICJzZWN1cml0eSI6ICJhdXRvIiwKICAgICJza2lwLWNlcnQtdmVyaWZ5IjogdHJ1ZSwKICAgICJzbmkiOiAiIgp9
    ss://Y2hhY2hhMjAtaWV0Zi1wb2x5MTMwNTphNDRlNjc4ZC01NDNlLTQ5ZTItOGNiNy0zOTk5ZTRmY2U1OTI=@free.2apzhfa.xyz:31243#%F0%9F%87%A8%F0%9F%87%B3CN-120.232.218.106-056
    ss://Y2hhY2hhMjAtaWV0Zi1wb2x5MTMwNTphNDRlNjc4ZC01NDNlLTQ5ZTItOGNiNy0zOTk5ZTRmY2U1OTI=@free.2apzhfa.xyz:31245#%F0%9F%87%A8%F0%9F%87%B3CN-120.232.218.106-057
    ss://Y2hhY2hhMjAtaWV0Zi1wb2x5MTMwNTphNDRlNjc4ZC01NDNlLTQ5ZTItOGNiNy0zOTk5ZTRmY2U1OTI=@free.2apzhfa.xyz:31111#%F0%9F%87%A8%F0%9F%87%B3CN-120.232.218.106-058
    ss://Y2hhY2hhMjAtaWV0Zi1wb2x5MTMwNTphNDRlNjc4ZC01NDNlLTQ5ZTItOGNiNy0zOTk5ZTRmY2U1OTI=@free.2apzhfa.xyz:31113#%F0%9F%87%A8%F0%9F%87%B3CN-120.232.218.106-059
    ss://Y2hhY2hhMjAtaWV0Zi1wb2x5MTMwNTphNDRlNjc4ZC01NDNlLTQ5ZTItOGNiNy0zOTk5ZTRmY2U1OTI=@free.2apzhfa.xyz:31115#%F0%9F%87%A8%F0%9F%87%B3CN-120.232.218.106-060
    ss://Y2hhY2hhMjAtaWV0Zi1wb2x5MTMwNTphNDRlNjc4ZC01NDNlLTQ5ZTItOGNiNy0zOTk5ZTRmY2U1OTI=@free.2apzhfa.xyz:31171#%F0%9F%87%A8%F0%9F%87%B3CN-120.232.218.106-061
    vmess://ewogICAgImFkZCI6ICJtcGRlLmNsb3VkZmxhcmUuMTgyNjgyLnh5eiIsCiAgICAiYWlkIjogMCwKICAgICJob3N0IjogInYyZGUxLjMzMzc4OS54eXoiLAogICAgImlkIjogImJhY2ZjZGYzLWFiYzEtMzhlZS05YTcwLTZjZmJjNzI2MjFjNyIsCiAgICAibmV0IjogIndzIiwKICAgICJwYXRoIjogIi9obHMvY2N0djVwaGQubTN1OCIsCiAgICAicG9ydCI6IDQ0MywKICAgICJwcyI6ICLwn4+BUkVMQVktMTA0LjE3LjIyMS4yNDgtMTg5IiwKICAgICJ0bHMiOiAidGxzIiwKICAgICJ0eXBlIjogImF1dG8iLAogICAgInNlY3VyaXR5IjogImF1dG8iLAogICAgInNraXAtY2VydC12ZXJpZnkiOiB0cnVlLAogICAgInNuaSI6ICIiCn0=
    ss://Y2hhY2hhMjAtaWV0Zi1wb2x5MTMwNTphNDRlNjc4ZC01NDNlLTQ5ZTItOGNiNy0zOTk5ZTRmY2U1OTI=@free.2apzhfa.xyz:31175#%F0%9F%87%A8%F0%9F%87%B3CN-120.232.218.106-063
    ss://Y2hhY2hhMjAtaWV0Zi1wb2x5MTMwNTphNDRlNjc4ZC01NDNlLTQ5ZTItOGNiNy0zOTk5ZTRmY2U1OTI=@free.2apzhfa.xyz:31311#%F0%9F%87%A8%F0%9F%87%B3CN-120.232.218.106-064
    ss://Y2hhY2hhMjAtaWV0Zi1wb2x5MTMwNTphNDRlNjc4ZC01NDNlLTQ5ZTItOGNiNy0zOTk5ZTRmY2U1OTI=@free.2apzhfa.xyz:31313#%F0%9F%87%A8%F0%9F%87%B3CN-120.232.218.106-065
    ss://Y2hhY2hhMjAtaWV0Zi1wb2x5MTMwNTphNDRlNjc4ZC01NDNlLTQ5ZTItOGNiNy0zOTk5ZTRmY2U1OTI=@free.2apzhfa.xyz:31341#%F0%9F%87%A8%F0%9F%87%B3CN-120.232.218.106-066
    ss://Y2hhY2hhMjAtaWV0Zi1wb2x5MTMwNTphNDRlNjc4ZC01NDNlLTQ5ZTItOGNiNy0zOTk5ZTRmY2U1OTI=@free.2apzhfa.xyz:31211#%F0%9F%87%A8%F0%9F%87%B3CN-120.232.218.106-067
    ss://Y2hhY2hhMjAtaWV0Zi1wb2x5MTMwNTphNDRlNjc4ZC01NDNlLTQ5ZTItOGNiNy0zOTk5ZTRmY2U1OTI=@free.2apzhfa.xyz:31213#%F0%9F%87%A8%F0%9F%87%B3CN-120.232.218.106-068
    ss://Y2hhY2hhMjAtaWV0Zi1wb2x5MTMwNTphNDRlNjc4ZC01NDNlLTQ5ZTItOGNiNy0zOTk5ZTRmY2U1OTI=@free.2apzhfa.xyz:31215#%F0%9F%87%A8%F0%9F%87%B3CN-120.232.218.106-069
    ss://Y2hhY2hhMjAtaWV0Zi1wb2x5MTMwNTphNDRlNjc4ZC01NDNlLTQ5ZTItOGNiNy0zOTk5ZTRmY2U1OTI=@free.2apzhfa.xyz:31271#%F0%9F%87%A8%F0%9F%87%B3CN-120.232.218.106-070
    ss://Y2hhY2hhMjAtaWV0Zi1wb2x5MTMwNTphNDRlNjc4ZC01NDNlLTQ5ZTItOGNiNy0zOTk5ZTRmY2U1OTI=@free.2apzhfa.xyz:31741#%F0%9F%87%A8%F0%9F%87%B3CN-120.232.218.106-071
    vmess://ewogICAgImFkZCI6ICI1OS40Mi4yNDcuMTg5IiwKICAgICJhaWQiOiAwLAogICAgImhvc3QiOiAid3d3LmJpbmcuY29tIiwKICAgICJpZCI6ICJkZDcyMmU4Ni02Y2VjLTQ0ZTgtYTQ0NC03ZjUxM2FiNjFjMGMiLAogICAgIm5ldCI6ICJ3cyIsCiAgICAicGF0aCI6ICIvbm1raiIsCiAgICAicG9ydCI6IDgwMDQsCiAgICAicHMiOiAi8J+HqPCfh7NDTi01OS40Mi4yNDcuMTg5LTE5MiIsCiAgICAidGxzIjogIiIsCiAgICAidHlwZSI6ICJhdXRvIiwKICAgICJzZWN1cml0eSI6ICJhdXRvIiwKICAgICJza2lwLWNlcnQtdmVyaWZ5IjogdHJ1ZSwKICAgICJzbmkiOiAiIgp9
    ss://Y2hhY2hhMjAtaWV0Zi1wb2x5MTMwNTphNDRlNjc4ZC01NDNlLTQ5ZTItOGNiNy0zOTk5ZTRmY2U1OTI=@free.2apzhfa.xyz:31722#%F0%9F%87%A8%F0%9F%87%B3CN-120.232.218.106-073
    ss://Y2hhY2hhMjAtaWV0Zi1wb2x5MTMwNTphNDRlNjc4ZC01NDNlLTQ5ZTItOGNiNy0zOTk5ZTRmY2U1OTI=@free.2apzhfa.xyz:31371#%F0%9F%87%A8%F0%9F%87%B3CN-120.232.218.106-074
    ss://Y2hhY2hhMjAtaWV0Zi1wb2x5MTMwNTphNDRlNjc4ZC01NDNlLTQ5ZTItOGNiNy0zOTk5ZTRmY2U1OTI=@free.2apzhfa.xyz:31411#%F0%9F%87%A8%F0%9F%87%B3CN-120.232.218.106-075
    ss://Y2hhY2hhMjAtaWV0Zi1wb2x5MTMwNTphNDRlNjc4ZC01NDNlLTQ5ZTItOGNiNy0zOTk5ZTRmY2U1OTI=@free.2apzhfa.xyz:31441#%F0%9F%87%A8%F0%9F%87%B3CN-120.232.218.106-076
    vmess://ewogICAgImFkZCI6ICJ2OC5oZWR1aWFuLmxpbmsiLAogICAgImFpZCI6IDIsCiAgICAiaG9zdCI6ICJ2OC5oZWR1aWFuLmxpbmsiLAogICAgImlkIjogImNiYjNmODc3LWQxZmItMzQ0Yy04N2E5LWQxNTNiZmZkNTQ4NCIsCiAgICAibmV0IjogIndzIiwKICAgICJwYXRoIjogIi9vb29vIiwKICAgICJwb3J0IjogMzA4MDgsCiAgICAicHMiOiAi8J+HqPCfh7NDTi0xMTEuMjYuMTA5Ljc5LTAwMCIsCiAgICAidGxzIjogIiIsCiAgICAidHlwZSI6ICJhdXRvIiwKICAgICJzZWN1cml0eSI6ICJhdXRvIiwKICAgICJza2lwLWNlcnQtdmVyaWZ5IjogdHJ1ZSwKICAgICJzbmkiOiAiIgp9
    ss://Y2hhY2hhMjAtaWV0Zi1wb2x5MTMwNTphNDRlNjc4ZC01NDNlLTQ5ZTItOGNiNy0zOTk5ZTRmY2U1OTI=@free.2apzhfa.xyz:31511#%F0%9F%87%A8%F0%9F%87%B3CN-120.232.218.106-078
    ss://Y2hhY2hhMjAtaWV0Zi1wb2x5MTMwNTphNDRlNjc4ZC01NDNlLTQ5ZTItOGNiNy0zOTk5ZTRmY2U1OTI=@free.2apzhfa.xyz:31571#%F0%9F%87%A8%F0%9F%87%B3CN-120.232.218.106-079
    ss://Y2hhY2hhMjAtaWV0Zi1wb2x5MTMwNTphNDRlNjc4ZC01NDNlLTQ5ZTItOGNiNy0zOTk5ZTRmY2U1OTI=@free.2apzhfa.xyz:31611#%F0%9F%87%A8%F0%9F%87%B3CN-120.232.218.106-080
    ss://Y2hhY2hhMjAtaWV0Zi1wb2x5MTMwNTphNDRlNjc4ZC01NDNlLTQ5ZTItOGNiNy0zOTk5ZTRmY2U1OTI=@free.2apzhfa.xyz:31641#%F0%9F%87%A8%F0%9F%87%B3CN-120.232.218.106-081
    ss://Y2hhY2hhMjAtaWV0Zi1wb2x5MTMwNTphNDRlNjc4ZC01NDNlLTQ5ZTItOGNiNy0zOTk5ZTRmY2U1OTI=@free.2apzhfa.xyz:31671#%F0%9F%87%A8%F0%9F%87%B3CN-120.232.218.106-082
    ss://Y2hhY2hhMjAtaWV0Zi1wb2x5MTMwNTphNDRlNjc4ZC01NDNlLTQ5ZTItOGNiNy0zOTk5ZTRmY2U1OTI=@free.2apzhfa.xyz:31677#%F0%9F%87%A8%F0%9F%87%B3CN-120.232.218.106-083
    ss://Y2hhY2hhMjAtaWV0Zi1wb2x5MTMwNTo2NWJkNmI4Zi00YTgyLTRlOTItOWUwNy1mMTRkMWUwYzgxMmE=@free.2weradf.xyz:36141#%F0%9F%87%A8%F0%9F%87%B3CN-120.232.218.106-084
    ss://Y2hhY2hhMjAtaWV0Zi1wb2x5MTMwNTo2NWJkNmI4Zi00YTgyLTRlOTItOWUwNy1mMTRkMWUwYzgxMmE=@free.2weradf.xyz:36143#%F0%9F%87%A8%F0%9F%87%B3CN-120.232.218.106-085
    ss://Y2hhY2hhMjAtaWV0Zi1wb2x5MTMwNTo2NWJkNmI4Zi00YTgyLTRlOTItOWUwNy1mMTRkMWUwYzgxMmE=@free.2weradf.xyz:36145#%F0%9F%87%A8%F0%9F%87%B3CN-120.232.218.106-086
    ss://Y2hhY2hhMjAtaWV0Zi1wb2x5MTMwNTo2NWJkNmI4Zi00YTgyLTRlOTItOWUwNy1mMTRkMWUwYzgxMmE=@free.2weradf.xyz:36241#%F0%9F%87%A8%F0%9F%87%B3CN-120.232.218.106-087
    ss://Y2hhY2hhMjAtaWV0Zi1wb2x5MTMwNTo2NWJkNmI4Zi00YTgyLTRlOTItOWUwNy1mMTRkMWUwYzgxMmE=@free.2weradf.xyz:36243#%F0%9F%87%A8%F0%9F%87%B3CN-120.232.218.106-088
    ss://Y2hhY2hhMjAtaWV0Zi1wb2x5MTMwNTo2NWJkNmI4Zi00YTgyLTRlOTItOWUwNy1mMTRkMWUwYzgxMmE=@free.2weradf.xyz:36245#%F0%9F%87%A8%F0%9F%87%B3CN-120.232.218.106-089
    ss://Y2hhY2hhMjAtaWV0Zi1wb2x5MTMwNTo2NWJkNmI4Zi00YTgyLTRlOTItOWUwNy1mMTRkMWUwYzgxMmE=@free.2weradf.xyz:36111#%F0%9F%87%A8%F0%9F%87%B3CN-120.232.218.106-090
    ss://Y2hhY2hhMjAtaWV0Zi1wb2x5MTMwNTo2NWJkNmI4Zi00YTgyLTRlOTItOWUwNy1mMTRkMWUwYzgxMmE=@free.2weradf.xyz:36113#%F0%9F%87%A8%F0%9F%87%B3CN-120.232.218.106-091
    ss://Y2hhY2hhMjAtaWV0Zi1wb2x5MTMwNTo2NWJkNmI4Zi00YTgyLTRlOTItOWUwNy1mMTRkMWUwYzgxMmE=@free.2weradf.xyz:36115#%F0%9F%87%A8%F0%9F%87%B3CN-120.232.218.106-092
    ss://Y2hhY2hhMjAtaWV0Zi1wb2x5MTMwNTo2NWJkNmI4Zi00YTgyLTRlOTItOWUwNy1mMTRkMWUwYzgxMmE=@free.2weradf.xyz:36171#%F0%9F%87%A8%F0%9F%87%B3CN-120.232.218.106-093
    ss://Y2hhY2hhMjAtaWV0Zi1wb2x5MTMwNTo2NWJkNmI4Zi00YTgyLTRlOTItOWUwNy1mMTRkMWUwYzgxMmE=@free.2weradf.xyz:36173#%F0%9F%87%A8%F0%9F%87%B3CN-120.232.218.106-094
    ss://Y2hhY2hhMjAtaWV0Zi1wb2x5MTMwNTo2NWJkNmI4Zi00YTgyLTRlOTItOWUwNy1mMTRkMWUwYzgxMmE=@free.2weradf.xyz:36311#%F0%9F%87%A8%F0%9F%87%B3CN-120.232.218.106-095
    ss://Y2hhY2hhMjAtaWV0Zi1wb2x5MTMwNTo2NWJkNmI4Zi00YTgyLTRlOTItOWUwNy1mMTRkMWUwYzgxMmE=@free.2weradf.xyz:36341#%F0%9F%87%A8%F0%9F%87%B3CN-120.232.218.106-096
    ss://Y2hhY2hhMjAtaWV0Zi1wb2x5MTMwNTo2NWJkNmI4Zi00YTgyLTRlOTItOWUwNy1mMTRkMWUwYzgxMmE=@free.2weradf.xyz:36211#%F0%9F%87%A8%F0%9F%87%B3CN-120.232.218.106-097
    ss://Y2hhY2hhMjAtaWV0Zi1wb2x5MTMwNTo2NWJkNmI4Zi00YTgyLTRlOTItOWUwNy1mMTRkMWUwYzgxMmE=@free.2weradf.xyz:36213#%F0%9F%87%A8%F0%9F%87%B3CN-120.232.218.106-098
    ss://Y2hhY2hhMjAtaWV0Zi1wb2x5MTMwNTo2NWJkNmI4Zi00YTgyLTRlOTItOWUwNy1mMTRkMWUwYzgxMmE=@free.2weradf.xyz:36215#%F0%9F%87%A8%F0%9F%87%B3CN-120.232.218.106-099
    ss://Y2hhY2hhMjAtaWV0Zi1wb2x5MTMwNTo2NWJkNmI4Zi00YTgyLTRlOTItOWUwNy1mMTRkMWUwYzgxMmE=@free.2weradf.xyz:36271#%F0%9F%87%A8%F0%9F%87%B3CN-120.232.218.106-100
    ss://Y2hhY2hhMjAtaWV0Zi1wb2x5MTMwNTo2NWJkNmI4Zi00YTgyLTRlOTItOWUwNy1mMTRkMWUwYzgxMmE=@free.2weradf.xyz:36721#%F0%9F%87%A8%F0%9F%87%B3CN-120.232.218.106-101
    ss://Y2hhY2hhMjAtaWV0Zi1wb2x5MTMwNTo2NWJkNmI4Zi00YTgyLTRlOTItOWUwNy1mMTRkMWUwYzgxMmE=@free.2weradf.xyz:36722#%F0%9F%87%A8%F0%9F%87%B3CN-120.232.218.106-102
    ss://Y2hhY2hhMjAtaWV0Zi1wb2x5MTMwNTo2NWJkNmI4Zi00YTgyLTRlOTItOWUwNy1mMTRkMWUwYzgxMmE=@free.2weradf.xyz:36741#%F0%9F%87%A8%F0%9F%87%B3CN-120.232.218.106-103
    ss://Y2hhY2hhMjAtaWV0Zi1wb2x5MTMwNTo2NWJkNmI4Zi00YTgyLTRlOTItOWUwNy1mMTRkMWUwYzgxMmE=@free.2weradf.xyz:36731#%F0%9F%87%A8%F0%9F%87%B3CN-120.232.218.106-104
    ss://Y2hhY2hhMjAtaWV0Zi1wb2x5MTMwNTo2NWJkNmI4Zi00YTgyLTRlOTItOWUwNy1mMTRkMWUwYzgxMmE=@free.2weradf.xyz:36371#%F0%9F%87%A8%F0%9F%87%B3CN-120.232.218.106-105
    ss://Y2hhY2hhMjAtaWV0Zi1wb2x5MTMwNTo2NWJkNmI4Zi00YTgyLTRlOTItOWUwNy1mMTRkMWUwYzgxMmE=@free.2weradf.xyz:36411#%F0%9F%87%A8%F0%9F%87%B3CN-120.232.218.106-106
    ss://Y2hhY2hhMjAtaWV0Zi1wb2x5MTMwNTo2NWJkNmI4Zi00YTgyLTRlOTItOWUwNy1mMTRkMWUwYzgxMmE=@free.2weradf.xyz:36441#%F0%9F%87%A8%F0%9F%87%B3CN-120.232.218.106-107
    ss://Y2hhY2hhMjAtaWV0Zi1wb2x5MTMwNTo2NWJkNmI4Zi00YTgyLTRlOTItOWUwNy1mMTRkMWUwYzgxMmE=@free.2weradf.xyz:36471#%F0%9F%87%A8%F0%9F%87%B3CN-120.232.218.106-108
    ss://Y2hhY2hhMjAtaWV0Zi1wb2x5MTMwNTo2NWJkNmI4Zi00YTgyLTRlOTItOWUwNy1mMTRkMWUwYzgxMmE=@free.2weradf.xyz:36511#%F0%9F%87%A8%F0%9F%87%B3CN-120.232.218.106-109
    ss://Y2hhY2hhMjAtaWV0Zi1wb2x5MTMwNTo2NWJkNmI4Zi00YTgyLTRlOTItOWUwNy1mMTRkMWUwYzgxMmE=@free.2weradf.xyz:36571#%F0%9F%87%A8%F0%9F%87%B3CN-120.232.218.106-110
    ss://Y2hhY2hhMjAtaWV0Zi1wb2x5MTMwNTo2NWJkNmI4Zi00YTgyLTRlOTItOWUwNy1mMTRkMWUwYzgxMmE=@free.2weradf.xyz:36611#%F0%9F%87%A8%F0%9F%87%B3CN-120.232.218.106-111
    ss://Y2hhY2hhMjAtaWV0Zi1wb2x5MTMwNTo2NWJkNmI4Zi00YTgyLTRlOTItOWUwNy1mMTRkMWUwYzgxMmE=@free.2weradf.xyz:36641#%F0%9F%87%A8%F0%9F%87%B3CN-120.232.218.106-112
    ss://Y2hhY2hhMjAtaWV0Zi1wb2x5MTMwNTo2NWJkNmI4Zi00YTgyLTRlOTItOWUwNy1mMTRkMWUwYzgxMmE=@free.2weradf.xyz:36671#%F0%9F%87%A8%F0%9F%87%B3CN-120.232.218.106-113
    ss://Y2hhY2hhMjAtaWV0Zi1wb2x5MTMwNTo2NWJkNmI4Zi00YTgyLTRlOTItOWUwNy1mMTRkMWUwYzgxMmE=@free.2weradf.xyz:36677#%F0%9F%87%A8%F0%9F%87%B3CN-120.232.218.106-114
    ss://YWVzLTI1Ni1jZmI6YXdzcHMwNTAx@57.180.41.89:443#%F0%9F%87%AF%F0%9F%87%B5JP-57.180.41.89-115
    trojan://a38c9e28-9960-4e31-9f18-ed2495a756aa@vt-bana2-cn-11.ghpgwqswodgzv.com:40021?security=tls&sni=vt-bana2-cn-11.ghpgwqswodgzv.com#%F0%9F%87%A8%F0%9F%87%B3CN-183.233.187.162-116
    ss://Y2hhY2hhMjAtaWV0Zi1wb2x5MTMwNTo5MWE0MWY0ZTAyZGM=@hkkh11v1.xpmc.cc:37512#%F0%9F%87%AD%F0%9F%87%B0HK-1.65.250.168-117
    trojan://d64c2ba8-0ae4-4299-8af7-8c5046e3c1c1@183.240.116.224:27102?security=tls&sni=q08m.vgraxiw73s.hasyaf.cn#%F0%9F%87%A8%F0%9F%87%B3CN-183.240.116.224-118
    trojan://VMhGp5wEIyCDf90T@csuzhou01.1cooldns.com:42303?security=tls&sni=hk06.run.place#%F0%9F%87%A8%F0%9F%87%B3CN-120.233.87.84-119
    ss://Y2hhY2hhMjAtaWV0Zi1wb2x5MTMwNTplZDBjYTBiZC0zYWEzLTRkM2EtODFiMC1lYWRjZDEwODNhNGQ=@xg-jd.huidu51.com:46603#%F0%9F%87%A8%F0%9F%87%B3CN-36.150.215.174-120
    ss://cmM0LW1kNTplZmFuY2N5dW4=@cn01.efan8867801.xyz:8766#%F0%9F%87%A8%F0%9F%87%B3CN-120.241.40.184-121
    ss://Y2hhY2hhMjAtaWV0Zi1wb2x5MTMwNTplZTAwM2M1ZmI4ZDg=@103.140.136.242:41827#%F0%9F%87%AF%F0%9F%87%B5JP-103.140.136.242-122
    vmess://ewogICAgImFkZCI6ICJ2MTIuaGVkdWlhbi5saW5rIiwKICAgICJhaWQiOiAyLAogICAgImhvc3QiOiAib2NiYy5jb20iLAogICAgImlkIjogImNiYjNmODc3LWQxZmItMzQ0Yy04N2E5LWQxNTNiZmZkNTQ4NCIsCiAgICAibmV0IjogIndzIiwKICAgICJwYXRoIjogIi9vb29vIiwKICAgICJwb3J0IjogMzA4MTIsCiAgICAicHMiOiAi8J+HqPCfh7NDTi0zNi4xNTAuOTQuMzUtMTIzIiwKICAgICJ0bHMiOiAiIiwKICAgICJ0eXBlIjogImF1dG8iLAogICAgInNlY3VyaXR5IjogImF1dG8iLAogICAgInNraXAtY2VydC12ZXJpZnkiOiB0cnVlLAogICAgInNuaSI6ICIiCn0=
    trojan://ce44b416-2d7e-49af-aa40-5a61d45f6fcc@58.254.186.222:27401?security=tls&sni=q08m.vgraxiw73s.hasyaf.cn#%F0%9F%87%A8%F0%9F%87%B3CN-58.254.186.222-124
    vmess://ewogICAgImFkZCI6ICJzZzYudmlwMi5nMi5tb29uYmFzZS5saWZlIiwKICAgICJhaWQiOiAwLAogICAgImhvc3QiOiAid2ViLnhjanMuaW5mbyIsCiAgICAiaWQiOiAiYzMxMzY4MTQtYTA3ZS00MWY2LWFkOTQtOGUyMDQ1OGMwZDIxIiwKICAgICJuZXQiOiAid3MiLAogICAgInBhdGgiOiAiL2hvbWUiLAogICAgInBvcnQiOiAzNTE0NiwKICAgICJwcyI6ICLwn4eo8J+Hs0NOLTE4My4yMzYuNTEuMTg3LTEyNSIsCiAgICAidGxzIjogInRscyIsCiAgICAidHlwZSI6ICJhdXRvIiwKICAgICJzZWN1cml0eSI6ICJhdXRvIiwKICAgICJza2lwLWNlcnQtdmVyaWZ5IjogZmFsc2UsCiAgICAic25pIjogIndlYi54Y2pzLmluZm8iCn0=
    vmess://ewogICAgImFkZCI6ICJ2MzIuaGVkdWlhbi5saW5rIiwKICAgICJhaWQiOiAyLAogICAgImhvc3QiOiAiYmFpZHUuY29tIiwKICAgICJpZCI6ICJjYmIzZjg3Ny1kMWZiLTM0NGMtODdhOS1kMTUzYmZmZDU0ODQiLAogICAgIm5ldCI6ICJ3cyIsCiAgICAicGF0aCI6ICIvb29vbyIsCiAgICAicG9ydCI6IDMwODMyLAogICAgInBzIjogIvCfh6jwn4ezQ04tMTExLjI2LjEwOS43OS0xMjYiLAogICAgInRscyI6ICIiLAogICAgInR5cGUiOiAiYXV0byIsCiAgICAic2VjdXJpdHkiOiAiYXV0byIsCiAgICAic2tpcC1jZXJ0LXZlcmlmeSI6IHRydWUsCiAgICAic25pIjogIiIKfQ==
    ss://cmM0LW1kNTplZmFuY2N5dW4=@cn01.efan8867801.xyz:8774#%F0%9F%87%A8%F0%9F%87%B3CN-120.241.40.184-127
    trojan://a8093ea8-f02e-4ffc-8a13-d068a62971bf@183.2.150.64:27301?security=tls&sni=q08m.vgraxiw73s.hasyaf.cn#%F0%9F%87%A8%F0%9F%87%B3CN-183.2.150.64-128
    vmess://ewogICAgImFkZCI6ICJ0ay5oemx0LnRrZGRucy54eXoiLAogICAgImFpZCI6IDIsCiAgICAiaG9zdCI6ICJ6eGpwLWIudGtvbmcuY2MiLAogICAgImlkIjogIjk4ZTk2YzlmLTRiYjMtMzlkNC05YTJjLWZhYzA0MjU3ZjdjNyIsCiAgICAibmV0IjogIndzIiwKICAgICJwYXRoIjogIi8iLAogICAgInBvcnQiOiAyMjY0MiwKICAgICJwcyI6ICLwn4eo8J+Hs0NOLTUyLjgwLjI3LjIyOS0xMjkiLAogICAgInRscyI6ICJ0bHMiLAogICAgInR5cGUiOiAiYXV0byIsCiAgICAic2VjdXJpdHkiOiAiYXV0byIsCiAgICAic2tpcC1jZXJ0LXZlcmlmeSI6IGZhbHNlLAogICAgInNuaSI6ICJ6eGpwLWIudGtvbmcuY2MiCn0=
    ss://YWVzLTI1Ni1jZmI6YXdzcHMwNTAx@3.112.233.244:443#%F0%9F%87%AF%F0%9F%87%B5JP-3.112.233.244-130
    ss://YWVzLTI1Ni1jZmI6YXdzcHMwNTAx@18.183.184.244:443#%F0%9F%87%AF%F0%9F%87%B5JP-18.183.184.244-131
    ss://YWVzLTI1Ni1jZmI6YXdzcHMwNTAx@54.199.249.6:443#%F0%9F%87%AF%F0%9F%87%B5JP-54.199.249.6-132
    vmess://ewogICAgImFkZCI6ICJzMS5jbi1kYi50b3AiLAogICAgImFpZCI6IDAsCiAgICAiaG9zdCI6ICIxMDAtNDctMTU0LTkuczEuY24tZGIudG9wIiwKICAgICJpZCI6ICI0YjM2NjI1Yy1iOWQ5LTNlYTYtYWVkNS04NmQ2MmM3MGUxNmQiLAogICAgIm5ldCI6ICJ3cyIsCiAgICAicGF0aCI6ICIvIiwKICAgICJwb3J0IjogMjA4NiwKICAgICJwcyI6ICLwn4+BUkVMQVktMTk4LjQxLjIwOS43MC0wMzUiLAogICAgInRscyI6ICIiLAogICAgInR5cGUiOiAiYXV0byIsCiAgICAic2VjdXJpdHkiOiAiYXV0byIsCiAgICAic2tpcC1jZXJ0LXZlcmlmeSI6IHRydWUsCiAgICAic25pIjogIiIKfQ==
    trojan://b6200af42ccadea353f5b5856dd20d70@113.99.140.184:39001?security=tls&sni=113.99.140.184#%F0%9F%87%A8%F0%9F%87%B3CN-113.99.140.184-135
    trojan://T%40_WvT8Ho%40LW%25w_%2C@172.66.47.42:2053?security=tls&sni=NOp-55q.pAgEs.dEv&type=ws&path=/trGPZDfetEwuO25SAs?ed=2560&Host=NOp-55q.pAgEs.dEv#%F0%9F%8F%81RELAY-172.66.47.42-034
    vmess://ewogICAgImFkZCI6ICIxMDQuMjEuMTYuMSIsCiAgICAiYWlkIjogMCwKICAgICJob3N0IjogInVzLmZyZWV5eWRzLmRwZG5zLm9yZyIsCiAgICAiaWQiOiAiMmYzOGY4NDgtYTg5OS00Yzg3LTk4MDctMjA3YTQxNjE1ZTNjIiwKICAgICJuZXQiOiAid3MiLAogICAgInBhdGgiOiAiL3JvbmdzZXZlbj9lZD0yMDQ4IiwKICAgICJwb3J0IjogODAsCiAgICAicHMiOiAi8J+PgVJFTEFZLTEwNC4yMS4xNi4xLTE0MyIsCiAgICAidGxzIjogIiIsCiAgICAidHlwZSI6ICJhdXRvIiwKICAgICJzZWN1cml0eSI6ICJhdXRvIiwKICAgICJza2lwLWNlcnQtdmVyaWZ5IjogdHJ1ZSwKICAgICJzbmkiOiAiIgp9
    trojan://cad5a49f-14e5-4a05-aae9-c5df8fad394f@172.67.157.220:443?security=tls&sni=c1sWER.777159.XYz#%F0%9F%8F%81RELAY-172.67.157.220-145
    trojan://Aimer@27.50.48.126:2083?security=tls&sni=tyep.esslh.filegear-sg.me#%F0%9F%8F%81RELAY-27.50.48.126-146
    vmess://ewogICAgImFkZCI6ICIxMDQuMTYuMTU1LjEwIiwKICAgICJhaWQiOiAwLAogICAgImhvc3QiOiAiMTAwLTE0OS0xOTEtMi5zNS5kYi1saW5rMDIudG9wIiwKICAgICJpZCI6ICI0YjM2NjI1Yy1iOWQ5LTNlYTYtYWVkNS04NmQ2MmM3MGUxNmQiLAogICAgIm5ldCI6ICJ3cyIsCiAgICAicGF0aCI6ICIvZGFiYWkuaW4xMDQuMjAuMTYuMjA5IiwKICAgICJwb3J0IjogODA4MCwKICAgICJwcyI6ICLwn4+BUkVMQVktMTA0LjE2LjE1NS4xMC0wMzMiLAogICAgInRscyI6ICIiLAogICAgInR5cGUiOiAiYXV0byIsCiAgICAic2VjdXJpdHkiOiAiYXV0byIsCiAgICAic2tpcC1jZXJ0LXZlcmlmeSI6IHRydWUsCiAgICAic25pIjogIiIKfQ==
    vmess://ewogICAgImFkZCI6ICJhZmx6enVsLm1laXF1YW5rb25namlhbi5jb20iLAogICAgImFpZCI6IDAsCiAgICAiaG9zdCI6ICJhZmx6enVsLm1laXF1YW5rb25namlhbi5jb20iLAogICAgImlkIjogIjM0MmJhY2ZkLTJiOGYtM2Y0OS1hMTZlLTQzOWRiNWIwYjlkNSIsCiAgICAibmV0IjogIndzIiwKICAgICJwYXRoIjogIi81NjRkZmEyMC8iLAogICAgInBvcnQiOiA1MTUxNSwKICAgICJwcyI6ICLwn4e68J+HuFVTLTM4LjE1MC4xMi4xODctMTQ5IiwKICAgICJ0bHMiOiAiIiwKICAgICJ0eXBlIjogImF1dG8iLAogICAgInNlY3VyaXR5IjogImF1dG8iLAogICAgInNraXAtY2VydC12ZXJpZnkiOiB0cnVlLAogICAgInNuaSI6ICIiCn0=
    trojan://67db0c34-ae7a-4369-a6b5-554c99d8e5c9@172.67.150.57:443?security=tls&sni=m4DdfG.999358.Xyz#%F0%9F%8F%81RELAY-172.67.150.57-152
    vmess://ewogICAgImFkZCI6ICIyMDIuNzguMTYyLjUiLAogICAgImFpZCI6IDAsCiAgICAiaG9zdCI6ICJpcnNvZnQuc3l0ZXMubmV0IiwKICAgICJpZCI6ICIyZmY5N2M2ZC04NTU3LTQyYTQtYjQzZi0xOWM3N2M1OTU5ZWEiLAogICAgIm5ldCI6ICJ3cyIsCiAgICAicGF0aCI6ICIvIiwKICAgICJwb3J0IjogNDQzLAogICAgInBzIjogIvCfh7nwn4e3VFItMjAyLjc4LjE2Mi41LTE1MyIsCiAgICAidGxzIjogInRscyIsCiAgICAidHlwZSI6ICJhdXRvIiwKICAgICJzZWN1cml0eSI6ICJhdXRvIiwKICAgICJza2lwLWNlcnQtdmVyaWZ5IjogdHJ1ZSwKICAgICJzbmkiOiAiIgp9
    trojan://15b24b56-d667-4fa8-b548-f3dc942fb461@172.67.173.64:443?security=tls&sni=d9032d6c-0ac0-4bdf-bd2f.2032.pp.ua#%F0%9F%8F%81RELAY-172.67.173.64-154
    trojan://cad5a49f-14e5-4a05-aae9-c5df8fad394f@104.21.14.54:443?security=tls&sni=C1Swew.777159.xyz#%F0%9F%8F%81RELAY-104.21.14.54-155
    trojan://4f435a3a-dfb8-4c90-b637-8df8c5d44550@172.67.135.37:443?security=tls&sni=m9rrrfgh.459.pp.ua#%F0%9F%8F%81RELAY-172.67.135.37-157
    trojan://67db0c34-ae7a-4369-a6b5-554c99d8e5c9@104.21.11.194:443?security=tls&sni=m4DdfG.999358.Xyz#%F0%9F%8F%81RELAY-104.21.11.194-158
    ss://Y2hhY2hhMjAtaWV0Zi1wb2x5MTMwNTozNlpDSGVhYlVTZktqZlFFdko0SERW@185.242.86.156:54170#%F0%9F%87%B3%F0%9F%87%B1NL-185.242.86.156-159
    trojan://8r%3C%5B9%27l6hAO%238ZQi@172.66.44.230:8443?security=tls&sni=Koma-YT.PAGeS.Dev&type=ws&path=/tro8sFW1S91B6sZrM1?ed=2560&Host=Koma-YT.PAGeS.Dev#%F0%9F%8F%81RELAY-172.66.44.230-032
    vmess://ewogICAgImFkZCI6ICJzNC5kYi1saW5rMDIudG9wIiwKICAgICJhaWQiOiAwLAogICAgImhvc3QiOiAiMTAwLTEyOC0xMi0xODAuczQuZGItbGluazAyLnRvcCIsCiAgICAiaWQiOiAiNGIzNjYyNWMtYjlkOS0zZWE2LWFlZDUtODZkNjJjNzBlMTZkIiwKICAgICJuZXQiOiAid3MiLAogICAgInBhdGgiOiAiL2RhYmFpLmluMTA0LjI1LjIzOS4xMzEiLAogICAgInBvcnQiOiA4ODgwLAogICAgInBzIjogIvCfj4FSRUxBWS0xOTguNDEuMjA5LjcwLTAzMSIsCiAgICAidGxzIjogIiIsCiAgICAidHlwZSI6ICJhdXRvIiwKICAgICJzZWN1cml0eSI6ICJhdXRvIiwKICAgICJza2lwLWNlcnQtdmVyaWZ5IjogdHJ1ZSwKICAgICJzbmkiOiAiIgp9
    vmess://ewogICAgImFkZCI6ICIxNTYuMjI5LjQ4LjIzNyIsCiAgICAiYWlkIjogMCwKICAgICJob3N0IjogImxheDEuaWJnZncudG9wIiwKICAgICJpZCI6ICIxOTFiYWJjNS0yYWFmLTRmZTUtYTU2My1mMTQyNDRhZWZiNGUiLAogICAgIm5ldCI6ICJ3cyIsCiAgICAicGF0aCI6ICIvIiwKICAgICJwb3J0IjogODQ0MywKICAgICJwcyI6ICLwn4+BUkVMQVktMTU2LjIyOS40OC4yMzctMDMwIiwKICAgICJ0bHMiOiAidGxzIiwKICAgICJ0eXBlIjogImF1dG8iLAogICAgInNlY3VyaXR5IjogImF1dG8iLAogICAgInNraXAtY2VydC12ZXJpZnkiOiB0cnVlLAogICAgInNuaSI6ICIiCn0=
    vmess://ewogICAgImFkZCI6ICJzMy5jbi1kYi50b3AiLAogICAgImFpZCI6IDAsCiAgICAiaG9zdCI6ICIxMDAtMTE5LTIxNS0xNTguczMuY24tZGIudG9wIiwKICAgICJpZCI6ICI0YjM2NjI1Yy1iOWQ5LTNlYTYtYWVkNS04NmQ2MmM3MGUxNmQiLAogICAgIm5ldCI6ICJ3cyIsCiAgICAicGF0aCI6ICIvIiwKICAgICJwb3J0IjogODA4MCwKICAgICJwcyI6ICLwn4+BUkVMQVktMTA0LjE5LjQ4LjIzNi0wMjkiLAogICAgInRscyI6ICIiLAogICAgInR5cGUiOiAiYXV0byIsCiAgICAic2VjdXJpdHkiOiAiYXV0byIsCiAgICAic2tpcC1jZXJ0LXZlcmlmeSI6IHRydWUsCiAgICAic25pIjogIiIKfQ==
    vmess://ewogICAgImFkZCI6ICIxMDQuMjEuNDQuMTg1IiwKICAgICJhaWQiOiAwLAogICAgImhvc3QiOiAiRnJlZWRvbWlzbmVhci5vbmV0d290aHJlZTEyMy5pciIsCiAgICAiaWQiOiAiODA4OGUyM2MtMjMzMi00NDIyLWM3NTQtOTI3NzI5YzU2OGJkIiwKICAgICJuZXQiOiAid3MiLAogICAgInBhdGgiOiAiL21laGRpIiwKICAgICJwb3J0IjogMjA1MiwKICAgICJwcyI6ICLwn4+BUkVMQVktMTA0LjIxLjQ0LjE4NS0wMjgiLAogICAgInRscyI6ICIiLAogICAgInR5cGUiOiAiYXV0byIsCiAgICAic2VjdXJpdHkiOiAiYXV0byIsCiAgICAic2tpcC1jZXJ0LXZlcmlmeSI6IHRydWUsCiAgICAic25pIjogIiIKfQ==
    vmess://ewogICAgImFkZCI6ICJzMS5kYi1saW5rMDEudG9wIiwKICAgICJhaWQiOiAwLAogICAgImhvc3QiOiAiMTAwLTE1MS0xNjQtNDcuczEuZGItbGluazAxLnRvcCIsCiAgICAiaWQiOiAiNGIzNjYyNWMtYjlkOS0zZWE2LWFlZDUtODZkNjJjNzBlMTZkIiwKICAgICJuZXQiOiAid3MiLAogICAgInBhdGgiOiAiL2RhYmFpLmluMTcyLjY3LjIuMTQyIiwKICAgICJwb3J0IjogMjA1MiwKICAgICJwcyI6ICLwn4+BUkVMQVktMTA0LjE3LjIyMS4yNDgtMDI3IiwKICAgICJ0bHMiOiAiIiwKICAgICJ0eXBlIjogImF1dG8iLAogICAgInNlY3VyaXR5IjogImF1dG8iLAogICAgInNraXAtY2VydC12ZXJpZnkiOiBmYWxzZSwKICAgICJzbmkiOiAiMTAwLTE1MS0xNjQtNDcuczEuZGItbGluazAxLnRvcCIKfQ==
    vmess://ewogICAgImFkZCI6ICIwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDgwLmNncm91cC1ub2RlLWZvci1iaWdhaXJwb3J0LnNicyIsCiAgICAiYWlkIjogMCwKICAgICJob3N0IjogIjAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwODAuY2dyb3VwLW5vZGUtZm9yLWJpZ2FpcnBvcnQuc2JzIiwKICAgICJpZCI6ICIzNTE5ZGZjMC1mYTI3LTQxY2MtOGMxOS05ODE4MThmOWY2ZDUiLAogICAgIm5ldCI6ICJ3cyIsCiAgICAicGF0aCI6ICIvIiwKICAgICJwb3J0IjogNDIzNjAsCiAgICAicHMiOiAi8J+HuvCfh7hVUy0zNC4yMjEuMTExLjE5Ny0wMjYiLAogICAgInRscyI6ICJ0bHMiLAogICAgInR5cGUiOiAiYXV0byIsCiAgICAic2VjdXJpdHkiOiAiYXV0byIsCiAgICAic2tpcC1jZXJ0LXZlcmlmeSI6IHRydWUsCiAgICAic25pIjogIiIKfQ==
    vmess://ewogICAgImFkZCI6ICIxNzIuNjcuNDIuMjMyIiwKICAgICJhaWQiOiAwLAogICAgImhvc3QiOiAidXMwM3MuNWQ4ZWNmODIuY2ZkIiwKICAgICJpZCI6ICI0YmYwNzRmNC03ZTljLTRlNGItYTEwZC0xNTZlMjYxOTk3MjkiLAogICAgIm5ldCI6ICJ3cyIsCiAgICAicGF0aCI6ICIvIiwKICAgICJwb3J0IjogODAsCiAgICAicHMiOiAi8J+PgVJFTEFZLTE3Mi42Ny40Mi4yMzItMDIzIiwKICAgICJ0bHMiOiAiIiwKICAgICJ0eXBlIjogImF1dG8iLAogICAgInNlY3VyaXR5IjogImF1dG8iLAogICAgInNraXAtY2VydC12ZXJpZnkiOiB0cnVlLAogICAgInNuaSI6ICIiCn0=
    vmess://ewogICAgImFkZCI6ICIxNzIuNjcuMTcyLjE2OCIsCiAgICAiYWlkIjogMCwKICAgICJob3N0IjogInVzMDNzLjVkOGVjZjgyLmNmZCIsCiAgICAiaWQiOiAiNGJmMDc0ZjQtN2U5Yy00ZTRiLWExMGQtMTU2ZTI2MTk5NzI5IiwKICAgICJuZXQiOiAid3MiLAogICAgInBhdGgiOiAiLyIsCiAgICAicG9ydCI6IDgwLAogICAgInBzIjogIvCfj4FSRUxBWS0xNzIuNjcuMTcyLjE2OC0wMjIiLAogICAgInRscyI6ICIiLAogICAgInR5cGUiOiAiYXV0byIsCiAgICAic2VjdXJpdHkiOiAiYXV0byIsCiAgICAic2tpcC1jZXJ0LXZlcmlmeSI6IHRydWUsCiAgICAic25pIjogIiIKfQ==
    trojan://15b24b56-d667-4fa8-b548-f3dc942fb461@104.21.34.159:443?security=tls&sni=2qwert.2031.pp.ua&type=ws&path=%2F4p35eUnmGxQ8YJFJxz&Host=2qwert.2031.pp.ua#%F0%9F%8F%81RELAY-104.21.34.159-169
    trojan://aa424865-2762-404c-b767-66c9f98e026b@104.21.83.113:443?security=tls&sni=X859886xYzX.859886.Xyz&type=ws&path=%2FP6OrM7FLvAhFqZdFGa29fCwxS&Host=X859886xYzX.859886.Xyz#%F0%9F%8F%81RELAY-104.21.83.113-173
    vmess://ewogICAgImFkZCI6ICIyMDIuNzguMTYyLjUiLAogICAgImFpZCI6IDAsCiAgICAiaG9zdCI6ICJzYWhhbmQuc2VydmVtaW5lY3JhZnQubmV0IiwKICAgICJpZCI6ICIxMTgyODdkMi1lOTY4LTQyZTEtODBkMC0xMmZhMmY1ZDM4ZDYiLAogICAgIm5ldCI6ICJ3cyIsCiAgICAicGF0aCI6ICIvIiwKICAgICJwb3J0IjogNDQzLAogICAgInBzIjogIvCfh7nwn4e3VFItMjAyLjc4LjE2Mi41LTE3NCIsCiAgICAidGxzIjogInRscyIsCiAgICAidHlwZSI6ICJhdXRvIiwKICAgICJzZWN1cml0eSI6ICJhdXRvIiwKICAgICJza2lwLWNlcnQtdmVyaWZ5IjogdHJ1ZSwKICAgICJzbmkiOiAiIgp9
    trojan://67db0c34-ae7a-4369-a6b5-554c99d8e5c9@104.21.86.106:443?security=tls&sni=M4rrT.999157.XYz&type=ws&path=%2FNuDL4mLrBwsbnEcmJLxC&Host=M4rrT.999157.XYz#%F0%9F%8F%81RELAY-104.21.86.106-176
    vmess://ewogICAgImFkZCI6ICI1OS40Mi4yNDcuMTg5IiwKICAgICJhaWQiOiAwLAogICAgImhvc3QiOiAid3d3LmJpbmcuY29tIiwKICAgICJpZCI6ICI1MDRhZWQ4NC1kOGU1LTQwNzYtYmJjMS0xNmExZTQyM2NkZjIiLAogICAgIm5ldCI6ICJ3cyIsCiAgICAicGF0aCI6ICIvbm1raiIsCiAgICAicG9ydCI6IDgwMDQsCiAgICAicHMiOiAi8J+HqPCfh7NDTi01OS40Mi4yNDcuMTg5LTE3NyIsCiAgICAidGxzIjogIiIsCiAgICAidHlwZSI6ICJhdXRvIiwKICAgICJzZWN1cml0eSI6ICJhdXRvIiwKICAgICJza2lwLWNlcnQtdmVyaWZ5IjogdHJ1ZSwKICAgICJzbmkiOiAiIgp9
    trojan://cad5a49f-14e5-4a05-aae9-c5df8fad394f@172.67.143.250:443?security=tls&sni=c1wsDmR.777162.XYz&type=ws&path=%2F5txgrUN3oqXENw4Z4&Host=c1wsDmR.777162.XYz#%F0%9F%8F%81RELAY-172.67.143.250-178
    trojan://4b132e2b-24b1-418b-90e9-a11b619a799b@104.21.82.14:443?security=tls&sni=m1assddr.777259.xyz&type=ws&path=%2FHnko4qt8WwmcpejJLlDlbpi&Host=m1assddr.777259.xyz#%F0%9F%8F%81RELAY-104.21.82.14-179
    vmess://ewogICAgImFkZCI6ICIxMDQuMjEuODIuMTgzIiwKICAgICJhaWQiOiAwLAogICAgImhvc3QiOiAic2VydmVyMjYuYmVoZXNodGJhbmVoLmNvbSIsCiAgICAiaWQiOiAiNWE3MDIxZTAtMjZiNC00NWQ2LWIxNzUtZmU1NTE2MDFjYTk3IiwKICAgICJuZXQiOiAid3MiLAogICAgInBhdGgiOiAiLyIsCiAgICAicG9ydCI6IDg4ODAsCiAgICAicHMiOiAi8J+PgVJFTEFZLTEwNC4yMS44Mi4xODMtMTgyIiwKICAgICJ0bHMiOiAiIiwKICAgICJ0eXBlIjogImF1dG8iLAogICAgInNlY3VyaXR5IjogImF1dG8iLAogICAgInNraXAtY2VydC12ZXJpZnkiOiB0cnVlLAogICAgInNuaSI6ICIiCn0=
    vmess://ewogICAgImFkZCI6ICJ2MjAuZW1veWVzLnRvcCIsCiAgICAiYWlkIjogMCwKICAgICJob3N0IjogInYyMC5lbW95ZXMudG9wIiwKICAgICJpZCI6ICJjMDUyNmM1Yi0zZTVmLTRmNzUtYTBlMi1mZmJhMzZiYjhlYmYiLAogICAgIm5ldCI6ICJ3cyIsCiAgICAicGF0aCI6ICIvIiwKICAgICJwb3J0IjogODQ0MywKICAgICJwcyI6ICLwn4+BUkVMQVktMTA0LjIxLjk2LjEtMTg0IiwKICAgICJ0bHMiOiAidGxzIiwKICAgICJ0eXBlIjogImF1dG8iLAogICAgInNlY3VyaXR5IjogImF1dG8iLAogICAgInNraXAtY2VydC12ZXJpZnkiOiB0cnVlLAogICAgInNuaSI6ICIiCn0=
    trojan://redfree8@104.17.147.22:443?security=tls&sni=ipsychO.SUEx12.Ir#%F0%9F%8F%81RELAY-104.17.147.22-185
    vmess://ewogICAgImFkZCI6ICJ0ay5oemx0LnRrZGRucy54eXoiLAogICAgImFpZCI6IDAsCiAgICAiaG9zdCI6ICIlN0IlMjJIb3N0JTIyOiUyMnp4anAtYi50a29uZy5jYyUyMiU3RCIsCiAgICAiaWQiOiAiOThlOTZjOWYtNGJiMy0zOWQ0LTlhMmMtZmFjMDQyNTdmN2M3IiwKICAgICJuZXQiOiAid3MiLAogICAgInBhdGgiOiAiLyIsCiAgICAicG9ydCI6IDIyNjQyLAogICAgInBzIjogIvCfh6jwn4ezQ04tNTIuODAuMjMyLjkzLTE4NyIsCiAgICAidGxzIjogInRscyIsCiAgICAidHlwZSI6ICJhdXRvIiwKICAgICJzZWN1cml0eSI6ICJhdXRvIiwKICAgICJza2lwLWNlcnQtdmVyaWZ5IjogdHJ1ZSwKICAgICJzbmkiOiAiIgp9
    vmess://ewogICAgImFkZCI6ICJtcHVzLmNsb3VkZmxhcmUuMTgyNjgyLnh5eiIsCiAgICAiYWlkIjogMCwKICAgICJob3N0IjogInYydXMyLjkwMjIyMi54eXoiLAogICAgImlkIjogImJhY2ZjZGYzLWFiYzEtMzhlZS05YTcwLTZjZmJjNzI2MjFjNyIsCiAgICAibmV0IjogIndzIiwKICAgICJwYXRoIjogIi9obHMvY2N0djVwaGQubTN1OCIsCiAgICAicG9ydCI6IDQ0MywKICAgICJwcyI6ICLwn4+BUkVMQVktMTA0LjE3LjIxMy4yNDEtMTg4IiwKICAgICJ0bHMiOiAidGxzIiwKICAgICJ0eXBlIjogImF1dG8iLAogICAgInNlY3VyaXR5IjogImF1dG8iLAogICAgInNraXAtY2VydC12ZXJpZnkiOiB0cnVlLAogICAgInNuaSI6ICIiCn0=
    ss://Y2hhY2hhMjAtaWV0Zi1wb2x5MTMwNTphNDRlNjc4ZC01NDNlLTQ5ZTItOGNiNy0zOTk5ZTRmY2U1OTI=@free.2apzhfa.xyz:31173#%F0%9F%87%A8%F0%9F%87%B3CN-120.232.218.106-062
    vmess://ewogICAgImFkZCI6ICJ0bHMuMDUubm9kZS1mb3ItYmlnYWlycG9ydC53aW4iLAogICAgImFpZCI6IDAsCiAgICAiaG9zdCI6ICJ0bHMuMDUubm9kZS1mb3ItYmlnYWlycG9ydC53aW4iLAogICAgImlkIjogImI3MWY5ZTg0LTg2YzktNDljNC1iNWY0LWIzM2IzNWVlNzQxMCIsCiAgICAibmV0IjogIndzIiwKICAgICJwYXRoIjogIi8iLAogICAgInBvcnQiOiAzMzQ0MywKICAgICJwcyI6ICLwn4ev8J+HtUpQLTEzLjIzMS4yMzYuMjU0LTAzOCIsCiAgICAidGxzIjogInRscyIsCiAgICAidHlwZSI6ICJhdXRvIiwKICAgICJzZWN1cml0eSI6ICJhdXRvIiwKICAgICJza2lwLWNlcnQtdmVyaWZ5IjogdHJ1ZSwKICAgICJzbmkiOiAiIgp9
    ss://Y2hhY2hhMjAtaWV0Zi1wb2x5MTMwNTphNDRlNjc4ZC01NDNlLTQ5ZTItOGNiNy0zOTk5ZTRmY2U1OTI=@free.2apzhfa.xyz:31721#%F0%9F%87%A8%F0%9F%87%B3CN-120.232.218.106-072
    vmess://ewogICAgImFkZCI6ICI1OS40Mi4yNDcuMTg5IiwKICAgICJhaWQiOiAwLAogICAgImhvc3QiOiAid3d3LmJpbmcuY29tIiwKICAgICJpZCI6ICI1OTg5YmY0NS1hOTljLTQ3NTQtOGZmMS03YzExNWQ5OGQyOTMiLAogICAgIm5ldCI6ICJ3cyIsCiAgICAicGF0aCI6ICIvbm1raiIsCiAgICAicG9ydCI6IDgwMDQsCiAgICAicHMiOiAi8J+HqPCfh7NDTi01OS40Mi4yNDcuMTg5LTE5NiIsCiAgICAidGxzIjogIiIsCiAgICAidHlwZSI6ICJhdXRvIiwKICAgICJzZWN1cml0eSI6ICJhdXRvIiwKICAgICJza2lwLWNlcnQtdmVyaWZ5IjogdHJ1ZSwKICAgICJzbmkiOiAiIgp9
    trojan://Aimer@27.50.48.126:2083?security=tls&sni=tyep.esslh.filegear-sg.me#%F0%9F%8F%81RELAY-27.50.48.126-290
    trojan://Aimer@219.76.13.177:443?security=tls&sni=tyep.esslh.filegear-sg.me#%F0%9F%87%AD%F0%9F%87%B0HK-219.76.13.177-291
    trojan://2c605663-b89a-5734-a9d6-97d4743d72cf@dozo01.flztjc.top:8313?security=tls&sni=hk-13-568.flztjc.net#%F0%9F%87%A8%F0%9F%87%B3CN-125.88.196.143-292
    trojan://2c605663-b89a-5734-a9d6-97d4743d72cf@183.232.235.2:8313?security=tls&sni=hk-13-568.flztjc.net#%F0%9F%87%A8%F0%9F%87%B3CN-183.232.235.2-293
    trojan://Aimer@92.243.74.180:8443?security=tls&sni=tyep.esslh.filegear-sg.me#%F0%9F%8F%81RELAY-92.243.74.180-301
    trojan://Aimer@14.63.60.134:50000?security=tls&sni=epccj.ambercc.filegear-sg.me#%F0%9F%87%B0%F0%9F%87%B7KR-14.63.60.134-307
    trojan://Aimer@121.135.236.180:12176?security=tls&sni=epccj.ambercc.filegear-sg.me#%F0%9F%87%B0%F0%9F%87%B7KR-121.135.236.180-308
    trojan://Aimer@222.114.124.22:35559?security=tls&sni=epccj.ambercc.filegear-sg.me#%F0%9F%87%B0%F0%9F%87%B7KR-222.114.124.22-309
    trojan://Aimer@arvind.ns.cloudflare.com:443?security=tls&sni=epccj.ambercc.filegear-sg.me#%F0%9F%8F%81RELAY-162.159.44.227-310
    trojan://Aimer@lynn.ns.cloudflare.com:443?security=tls&sni=epccj.ambercc.filegear-sg.me#%F0%9F%8F%81RELAY-172.64.33.201-311
    trojan://Aimer@92.243.74.180:8443?security=tls&sni=tyep.esslh.filegear-sg.me#%F0%9F%8F%81RELAY-92.243.74.180-315
    vmess://ewogICAgImFkZCI6ICI1OS40Mi4yNDcuMTg5IiwKICAgICJhaWQiOiAwLAogICAgImhvc3QiOiAiIiwKICAgICJpZCI6ICI3OGQ4NWMwYi00Y2M1LTRlNjEtOWQwZC1mM2JlNzNmZWM4NjMiLAogICAgIm5ldCI6ICJ3cyIsCiAgICAicGF0aCI6ICIvIiwKICAgICJwb3J0IjogODAwNCwKICAgICJwcyI6ICLwn4eo8J+Hs0NOLTU5LjQyLjI0Ny4xODktMzI0IiwKICAgICJ0bHMiOiAiIiwKICAgICJ0eXBlIjogImF1dG8iLAogICAgInNlY3VyaXR5IjogImF1dG8iLAogICAgInNraXAtY2VydC12ZXJpZnkiOiB0cnVlLAogICAgInNuaSI6ICIiCn0=
    vmess://ewogICAgImFkZCI6ICI1OS40Mi4yNDcuMTg5IiwKICAgICJhaWQiOiAwLAogICAgImhvc3QiOiAiIiwKICAgICJpZCI6ICI2ODI2MTY2Mi05ODJhLTQxYjUtOTRmZi1kYWQ0MDZhNDFjMDMiLAogICAgIm5ldCI6ICJ3cyIsCiAgICAicGF0aCI6ICIvIiwKICAgICJwb3J0IjogODAwNCwKICAgICJwcyI6ICLwn4eo8J+Hs0NOLTU5LjQyLjI0Ny4xODktMzI2IiwKICAgICJ0bHMiOiAiIiwKICAgICJ0eXBlIjogImF1dG8iLAogICAgInNlY3VyaXR5IjogImF1dG8iLAogICAgInNraXAtY2VydC12ZXJpZnkiOiB0cnVlLAogICAgInNuaSI6ICIiCn0=
    vmess://ewogICAgImFkZCI6ICJ2NDAuaGVkdWlhbi5saW5rIiwKICAgICJhaWQiOiAwLAogICAgImhvc3QiOiAidjQwLmhlZHVpYW4ubGluayIsCiAgICAiaWQiOiAiY2JiM2Y4NzctZDFmYi0zNDRjLTg3YTktZDE1M2JmZmQ1NDg0IiwKICAgICJuZXQiOiAid3MiLAogICAgInBhdGgiOiAiLyIsCiAgICAicG9ydCI6IDMwODQwLAogICAgInBzIjogIvCfh6jwn4ezQ04tMTExLjI2LjEwOS43OS0zMzAiLAogICAgInRscyI6ICIiLAogICAgInR5cGUiOiAiYXV0byIsCiAgICAic2VjdXJpdHkiOiAiYXV0byIsCiAgICAic2tpcC1jZXJ0LXZlcmlmeSI6IHRydWUsCiAgICAic25pIjogIiIKfQ==
    vmess://ewogICAgImFkZCI6ICI1OS40Mi4yNDcuMTg5IiwKICAgICJhaWQiOiAwLAogICAgImhvc3QiOiAiIiwKICAgICJpZCI6ICI2ODI2MTY2Mi05ODJhLTQxYjUtOTRmZi1kYWQ0MDZhNDFjMDMiLAogICAgIm5ldCI6ICJ3cyIsCiAgICAicGF0aCI6ICIvIiwKICAgICJwb3J0IjogODAwNCwKICAgICJwcyI6ICLwn4eo8J+Hs0NOLTU5LjQyLjI0Ny4xODktMzM0IiwKICAgICJ0bHMiOiAiIiwKICAgICJ0eXBlIjogImF1dG8iLAogICAgInNlY3VyaXR5IjogImF1dG8iLAogICAgInNraXAtY2VydC12ZXJpZnkiOiB0cnVlLAogICAgInNuaSI6ICIiCn0=
    vmess://ewogICAgImFkZCI6ICJrYXBlbGxlbmcuY29tIiwKICAgICJhaWQiOiAwLAogICAgImhvc3QiOiAia2FwZWxsZW5nLmNvbSIsCiAgICAiaWQiOiAiMDNmY2M2MTgtYjkzZC02Nzk2LTZhZWQtOGEzOGM5NzVkNTgxIiwKICAgICJuZXQiOiAid3MiLAogICAgInBhdGgiOiAiLyIsCiAgICAicG9ydCI6IDQ0MywKICAgICJwcyI6ICLwn4ep8J+HqkRFLTU3LjEyOS42NC4yMzgtMzQwIiwKICAgICJ0bHMiOiAiIiwKICAgICJ0eXBlIjogImF1dG8iLAogICAgInNlY3VyaXR5IjogImF1dG8iLAogICAgInNraXAtY2VydC12ZXJpZnkiOiB0cnVlLAogICAgInNuaSI6ICIiCn0=
    vmess://ewogICAgImFkZCI6ICI0NS4xNDcuMjAxLjIzMSIsCiAgICAiYWlkIjogMCwKICAgICJob3N0IjogIiIsCiAgICAiaWQiOiAiMWNjNTlhM2EtOTYyNS00MGY3LWIwZTYtZTIzMzI4NmFlODJkIiwKICAgICJuZXQiOiAid3MiLAogICAgInBhdGgiOiAiLyIsCiAgICAicG9ydCI6IDIyMDM2LAogICAgInBzIjogIvCfh7fwn4e6UlUtNDUuMTQ3LjIwMS4yMzEtMzQxIiwKICAgICJ0bHMiOiAiIiwKICAgICJ0eXBlIjogImF1dG8iLAogICAgInNlY3VyaXR5IjogImF1dG8iLAogICAgInNraXAtY2VydC12ZXJpZnkiOiB0cnVlLAogICAgInNuaSI6ICIiCn0=
    vmess://ewogICAgImFkZCI6ICIxMDQuMTguMTQ5Ljc1IiwKICAgICJhaWQiOiAwLAogICAgImhvc3QiOiAiIiwKICAgICJpZCI6ICJjYWU5N2IxYy0zNWU4LTRjZjItZGMxYi01MjAzMmMzZDNmYTciLAogICAgIm5ldCI6ICJ3cyIsCiAgICAicGF0aCI6ICIvIiwKICAgICJwb3J0IjogNDQzLAogICAgInBzIjogIvCfj4FSRUxBWS0xMDQuMTguMTQ5Ljc1LTM0MiIsCiAgICAidGxzIjogIiIsCiAgICAidHlwZSI6ICJhdXRvIiwKICAgICJzZWN1cml0eSI6ICJhdXRvIiwKICAgICJza2lwLWNlcnQtdmVyaWZ5IjogdHJ1ZSwKICAgICJzbmkiOiAiIgp9
    vmess://ewogICAgImFkZCI6ICJ2MzMuZW1veWVzLnRvcCIsCiAgICAiYWlkIjogMCwKICAgICJob3N0IjogInYzMy5lbW95ZXMudG9wIiwKICAgICJpZCI6ICJjMDUyNmM1Yi0zZTVmLTRmNzUtYTBlMi1mZmJhMzZiYjhlYmYiLAogICAgIm5ldCI6ICJ3cyIsCiAgICAicGF0aCI6ICIvIiwKICAgICJwb3J0IjogNDQzLAogICAgInBzIjogIvCfj4FSRUxBWS0xMDQuMjEuMTEyLjEtMzQzIiwKICAgICJ0bHMiOiAiIiwKICAgICJ0eXBlIjogImF1dG8iLAogICAgInNlY3VyaXR5IjogImF1dG8iLAogICAgInNraXAtY2VydC12ZXJpZnkiOiB0cnVlLAogICAgInNuaSI6ICIiCn0=
    vmess://ewogICAgImFkZCI6ICJib29rbXlzaG93LmNvbSIsCiAgICAiYWlkIjogMCwKICAgICJob3N0IjogImJvb2tteXNob3cuY29tIiwKICAgICJpZCI6ICI4MWFkMzcwZi00MjMxLTRhNjMtYWRlNS0yZDY3NzUyZWZkOGUiLAogICAgIm5ldCI6ICJ3cyIsCiAgICAicGF0aCI6ICIvIiwKICAgICJwb3J0IjogNDQzLAogICAgInBzIjogIvCfj4FSRUxBWS0xMDQuMTcuMTg5LjE5NS0zNDQiLAogICAgInRscyI6ICIiLAogICAgInR5cGUiOiAiYXV0byIsCiAgICAic2VjdXJpdHkiOiAiYXV0byIsCiAgICAic2tpcC1jZXJ0LXZlcmlmeSI6IHRydWUsCiAgICAic25pIjogIiIKfQ==
    vmess://ewogICAgImFkZCI6ICJ2MzUuZW1veWVzLnRvcCIsCiAgICAiYWlkIjogMCwKICAgICJob3N0IjogInYzNS5lbW95ZXMudG9wIiwKICAgICJpZCI6ICJjMDUyNmM1Yi0zZTVmLTRmNzUtYTBlMi1mZmJhMzZiYjhlYmYiLAogICAgIm5ldCI6ICJ3cyIsCiAgICAicGF0aCI6ICIvIiwKICAgICJwb3J0IjogNDQzLAogICAgInBzIjogIvCfj4FSRUxBWS0xMDQuMjEuNDguMS0zNDUiLAogICAgInRscyI6ICIiLAogICAgInR5cGUiOiAiYXV0byIsCiAgICAic2VjdXJpdHkiOiAiYXV0byIsCiAgICAic2tpcC1jZXJ0LXZlcmlmeSI6IHRydWUsCiAgICAic25pIjogIiIKfQ==
    vmess://ewogICAgImFkZCI6ICI5eC45MzgucHAudWEiLAogICAgImFpZCI6IDAsCiAgICAiaG9zdCI6ICI5eC45MzgucHAudWEiLAogICAgImlkIjogIjkwNmJhOTJmLWVmOTYtNDEzMy04ZWVlLWYzMzIwMmE1YTcyMSIsCiAgICAibmV0IjogIndzIiwKICAgICJwYXRoIjogIi8iLAogICAgInBvcnQiOiA0NDMsCiAgICAicHMiOiAi8J+PgVJFTEFZLTE3Mi42Ny4xNjkuOTEtMzQ2IiwKICAgICJ0bHMiOiAiIiwKICAgICJ0eXBlIjogImF1dG8iLAogICAgInNlY3VyaXR5IjogImF1dG8iLAogICAgInNraXAtY2VydC12ZXJpZnkiOiB0cnVlLAogICAgInNuaSI6ICIiCn0=
    vmess://ewogICAgImFkZCI6ICIxMDQuMjEuMTYuMSIsCiAgICAiYWlkIjogMCwKICAgICJob3N0IjogIiIsCiAgICAiaWQiOiAiMmYzOGY4NDgtYTg5OS00Yzg3LTk4MDctMjA3YTQxNjE1ZTNjIiwKICAgICJuZXQiOiAid3MiLAogICAgInBhdGgiOiAiLyIsCiAgICAicG9ydCI6IDgwLAogICAgInBzIjogIvCfj4FSRUxBWS0xMDQuMjEuMTYuMS0zNDciLAogICAgInRscyI6ICIiLAogICAgInR5cGUiOiAiYXV0byIsCiAgICAic2VjdXJpdHkiOiAiYXV0byIsCiAgICAic2tpcC1jZXJ0LXZlcmlmeSI6IHRydWUsCiAgICAic25pIjogIiIKfQ==
    vmess://ewogICAgImFkZCI6ICIxMDQuMjEuNjQuMSIsCiAgICAiYWlkIjogMCwKICAgICJob3N0IjogIiIsCiAgICAiaWQiOiAiMmYzOGY4NDgtYTg5OS00Yzg3LTk4MDctMjA3YTQxNjE1ZTNjIiwKICAgICJuZXQiOiAid3MiLAogICAgInBhdGgiOiAiLyIsCiAgICAicG9ydCI6IDgwLAogICAgInBzIjogIvCfj4FSRUxBWS0xMDQuMjEuNjQuMS0zNDgiLAogICAgInRscyI6ICIiLAogICAgInR5cGUiOiAiYXV0byIsCiAgICAic2VjdXJpdHkiOiAiYXV0byIsCiAgICAic2tpcC1jZXJ0LXZlcmlmeSI6IHRydWUsCiAgICAic25pIjogIiIKfQ==
    vmess://ewogICAgImFkZCI6ICI3ZmE1NDM0My03YzBhLTQ1YzkuMjAzMS5wcC51YSIsCiAgICAiYWlkIjogMCwKICAgICJob3N0IjogIjdmYTU0MzQzLTdjMGEtNDVjOS4yMDMxLnBwLnVhIiwKICAgICJpZCI6ICIxNWIyNGI1Ni1kNjY3LTRmYTgtYjU0OC1mM2RjOTQyZmI0NjEiLAogICAgIm5ldCI6ICJ3cyIsCiAgICAicGF0aCI6ICIvIiwKICAgICJwb3J0IjogNDQzLAogICAgInBzIjogIvCfj4FSRUxBWS0xNzIuNjcuMTYzLjE0LTM0OSIsCiAgICAidGxzIjogIiIsCiAgICAidHlwZSI6ICJhdXRvIiwKICAgICJzZWN1cml0eSI6ICJhdXRvIiwKICAgICJza2lwLWNlcnQtdmVyaWZ5IjogdHJ1ZSwKICAgICJzbmkiOiAiIgp9
    vmess://ewogICAgImFkZCI6ICI1MS43OS4xMDIuMjUzIiwKICAgICJhaWQiOiAwLAogICAgImhvc3QiOiAiIiwKICAgICJpZCI6ICI1OGZlMTU0Mi01MjkwLTQwYWQtODE1YS03NzcwN2E4MWFmZTUiLAogICAgIm5ldCI6ICJ3cyIsCiAgICAicGF0aCI6ICIvIiwKICAgICJwb3J0IjogODAsCiAgICAicHMiOiAi8J+HqPCfh6ZDQS01MS43OS4xMDIuMjUzLTM1MSIsCiAgICAidGxzIjogIiIsCiAgICAidHlwZSI6ICJhdXRvIiwKICAgICJzZWN1cml0eSI6ICJhdXRvIiwKICAgICJza2lwLWNlcnQtdmVyaWZ5IjogdHJ1ZSwKICAgICJzbmkiOiAiIgp9
    vmess://ewogICAgImFkZCI6ICIyZTIxY2VkYy1mYThiLTQwMjAtOGNlMC0zOTBlNzI4N2QyNzYuODkwNjAzLnBwLnVhIiwKICAgICJhaWQiOiAwLAogICAgImhvc3QiOiAiMmUyMWNlZGMtZmE4Yi00MDIwLThjZTAtMzkwZTcyODdkMjc2Ljg5MDYwMy5wcC51YSIsCiAgICAiaWQiOiAiNTQ1M2FlMjYtMjUwZC00ZTc5LWI0ZWMtMDE2YmFmODA2ODY1IiwKICAgICJuZXQiOiAid3MiLAogICAgInBhdGgiOiAiLyIsCiAgICAicG9ydCI6IDQ0MywKICAgICJwcyI6ICLwn4+BUkVMQVktMTA0LjIxLjcxLjIwNS0zNTIiLAogICAgInRscyI6ICIiLAogICAgInR5cGUiOiAiYXV0byIsCiAgICAic2VjdXJpdHkiOiAiYXV0byIsCiAgICAic2tpcC1jZXJ0LXZlcmlmeSI6IHRydWUsCiAgICAic25pIjogIiIKfQ==
    vmess://ewogICAgImFkZCI6ICIxMDQuMTYuMC4wIiwKICAgICJhaWQiOiAwLAogICAgImhvc3QiOiAiIiwKICAgICJpZCI6ICIwMWY3NWI2YS05MzVmLTQ2NmMtYmEzZC05ZjU2MWQ5YmYxOTEiLAogICAgIm5ldCI6ICJ3cyIsCiAgICAicGF0aCI6ICIvIiwKICAgICJwb3J0IjogNDQzLAogICAgInBzIjogIvCfj4FSRUxBWS0xMDQuMTYuMC4wLTM1MyIsCiAgICAidGxzIjogIiIsCiAgICAidHlwZSI6ICJhdXRvIiwKICAgICJzZWN1cml0eSI6ICJhdXRvIiwKICAgICJza2lwLWNlcnQtdmVyaWZ5IjogdHJ1ZSwKICAgICJzbmkiOiAiIgp9
    vmess://ewogICAgImFkZCI6ICI3ZmE1NDM0My03YzBhLTQ1YzkuMjAzMS5wcC51YSIsCiAgICAiYWlkIjogMCwKICAgICJob3N0IjogIjdmYTU0MzQzLTdjMGEtNDVjOS4yMDMxLnBwLnVhIiwKICAgICJpZCI6ICIxNWIyNGI1Ni1kNjY3LTRmYTgtYjU0OC1mM2RjOTQyZmI0NjEiLAogICAgIm5ldCI6ICJ3cyIsCiAgICAicGF0aCI6ICIvIiwKICAgICJwb3J0IjogNDQzLAogICAgInBzIjogIvCfj4FSRUxBWS0xNzIuNjcuMTYzLjE0LTM1NSIsCiAgICAidGxzIjogIiIsCiAgICAidHlwZSI6ICJhdXRvIiwKICAgICJzZWN1cml0eSI6ICJhdXRvIiwKICAgICJza2lwLWNlcnQtdmVyaWZ5IjogdHJ1ZSwKICAgICJzbmkiOiAiIgp9
    vmess://ewogICAgImFkZCI6ICIxNTguMTgwLjIyOC4yMjYiLAogICAgImFpZCI6IDAsCiAgICAiaG9zdCI6ICIiLAogICAgImlkIjogIjliNDU2YzJhLWYyYzEtNDVlMS04N2E5LWI3NjI4YjA0YmIyNCIsCiAgICAibmV0IjogIndzIiwKICAgICJwYXRoIjogIi8iLAogICAgInBvcnQiOiA0NDMsCiAgICAicHMiOiAi8J+HrvCfh7lJVC0xNTguMTgwLjIyOC4yMjYtMzU2IiwKICAgICJ0bHMiOiAiIiwKICAgICJ0eXBlIjogImF1dG8iLAogICAgInNlY3VyaXR5IjogImF1dG8iLAogICAgInNraXAtY2VydC12ZXJpZnkiOiB0cnVlLAogICAgInNuaSI6ICIiCn0=

    vmess://ewogICAgImFkZCI6ICJ3d3cuZ292LmhrIiwKICAgICJhaWQiOiAwLAogICAgImhvc3QiOiAibGludXMuY2xvdWRmbGFyZS5xdWVzdCIsCiAgICAiaWQiOiAiMWFiOTFmMTgtNjE2OC00Y2I2LWM5Y2EtMmMzYzcxNThmZTRjIiwKICAgICJuZXQiOiAid3MiLAogICAgInBhdGgiOiAiL2FyaWVzIiwKICAgICJwb3J0IjogMjA4NiwKICAgICJwcyI6ICLwn4+BUkVMQVktMTA0LjE2LjI0OS4xMzAtMTMwMSIsCiAgICAidGxzIjogIiIsCiAgICAidHlwZSI6ICJhdXRvIiwKICAgICJzZWN1cml0eSI6ICJhdXRvIiwKICAgICJza2lwLWNlcnQtdmVyaWZ5IjogdHJ1ZSwKICAgICJzbmkiOiAiIgp9
    ss://YWVzLTEyOC1jZmI6c2hhZG93c29ja3M=@156.146.38.163:443#%F0%9F%87%BA%F0%9F%87%B8US-156.146.38.163-0799
    vmess://ewogICAgImFkZCI6ICJ4ci0xLmhlcm9rdWFwcC5jb20iLAogICAgImFpZCI6IDAsCiAgICAiaG9zdCI6ICJ4ci0xLmhlcm9rdWFwcC5jb20iLAogICAgImlkIjogIjE3YWY3NmUxLWE1ZDctNDFhYi1hZTg3LWI0OGYxODUwNzVkMSIsCiAgICAibmV0IjogIndzIiwKICAgICJwYXRoIjogIi8xN2FmNzZlMS1hNWQ3LTQxYWItYWU4Ny1iNDhmMTg1MDc1ZDEtdm1lc3MiLAogICAgInBvcnQiOiA0NDMsCiAgICAicHMiOiAi8J+HuvCfh7hVUy01NC4yNDMuMTI5LjIxNS0xOTA1MCIsCiAgICAidGxzIjogInRscyIsCiAgICAidHlwZSI6ICJhdXRvIiwKICAgICJzZWN1cml0eSI6ICJhdXRvIiwKICAgICJza2lwLWNlcnQtdmVyaWZ5IjogdHJ1ZSwKICAgICJzbmkiOiAiIgp9
    ss://YWVzLTI1Ni1jZmI6Yndoc2tyc2tyMDM=@172.96.192.58:254#%F0%9F%87%BA%F0%9F%87%B8US-172.96.192.58-0463
    ss://YWVzLTI1Ni1jZmI6Yndoc2tyc2tyMDM=@97.64.31.80:247#%F0%9F%87%BA%F0%9F%87%B8US-97.64.31.80-0461
    ss://YWVzLTI1Ni1jZmI6Yndoc2tyc2tyMDM=@144.168.60.70:252#%F0%9F%87%BA%F0%9F%87%B8US-144.168.60.70-15607
    vmess://ewogICAgImFkZCI6ICIxNDEuMTAxLjExNC4yMCIsCiAgICAiYWlkIjogMCwKICAgICJob3N0IjogImNsYXNoMS50cnVtcDIwMjMubmV0IiwKICAgICJpZCI6ICIxNzZiNTk4Zi00NDViLTQxYWMtOWQyYS00MzBjNWM0ZGYyNmEiLAogICAgIm5ldCI6ICJ3cyIsCiAgICAicGF0aCI6ICIvZG9uZ3RhaXdhbmcuY29tIiwKICAgICJwb3J0IjogNDQzLAogICAgInBzIjogIvCfj4FSRUxBWS0xNDEuMTAxLjExNC4yMC0wMjk0IiwKICAgICJ0bHMiOiAidGxzIiwKICAgICJ0eXBlIjogImF1dG8iLAogICAgInNlY3VyaXR5IjogImF1dG8iLAogICAgInNraXAtY2VydC12ZXJpZnkiOiB0cnVlLAogICAgInNuaSI6ICIiCn0=
    ss://YWVzLTI1Ni1jZmI6Yndoc2tyc2tyMDU=@172.96.192.100:246#%F0%9F%87%BA%F0%9F%87%B8US-172.96.192.100-15615
    vmess://ewogICAgImFkZCI6ICI2Ny4yMS43Mi40MSIsCiAgICAiYWlkIjogNjQsCiAgICAiaG9zdCI6ICJ3d3cuMTcwODAxMDAueHl6IiwKICAgICJpZCI6ICIyNTY2ZDAwZi0yMThjLTQ4ZjctOWEzNi0xM2QzZDZmMWE3MjQiLAogICAgIm5ldCI6ICJ3cyIsCiAgICAicGF0aCI6ICIvcGF0aC8xNzM0MTgxNDExMjMiLAogICAgInBvcnQiOiA0NDMsCiAgICAicHMiOiAi8J+HuvCfh7hVUy02Ny4yMS43Mi40MS01NTE4IiwKICAgICJ0bHMiOiAidGxzIiwKICAgICJ0eXBlIjogImF1dG8iLAogICAgInNlY3VyaXR5IjogImF1dG8iLAogICAgInNraXAtY2VydC12ZXJpZnkiOiB0cnVlLAogICAgInNuaSI6ICIiCn0=
    ss://YWVzLTI1Ni1jZmI6Yndoc2tyc2tyMDY=@95.169.4.174:254#%F0%9F%87%BA%F0%9F%87%B8US-95.169.4.174-15616
    ss://YWVzLTI1Ni1jZmI6Yndoc2tyc2tyMDM=@104.243.25.95:253#%F0%9F%87%BA%F0%9F%87%B8US-104.243.25.95-0436
    ss://YWVzLTI1Ni1jZmI6Yndoc2tyc2tyMDU=@144.168.58.170:254#%F0%9F%87%BA%F0%9F%87%B8US-144.168.58.170-15618
    ss://YWVzLTI1Ni1jZmI6Yndoc2tyc2tyMDU=@107.182.177.136:256#%F0%9F%87%BA%F0%9F%87%B8US-107.182.177.136-0659
    ss://YWVzLTI1Ni1jZmI6Yndoc2tyc2tyMDY=@93.179.112.70:253#%F0%9F%87%BA%F0%9F%87%B8US-93.179.112.70-15619
    vmess://ewogICAgImFkZCI6ICI2Ny4yMS43Mi40MSIsCiAgICAiYWlkIjogNjQsCiAgICAiaG9zdCI6ICI2Ny4yMS43Mi40MSIsCiAgICAiaWQiOiAiMjU2NmQwMGYtMjE4Yy00OGY3LTlhMzYtMTNkM2Q2ZjFhNzI0IiwKICAgICJuZXQiOiAid3MiLAogICAgInBhdGgiOiAiL3BhdGgvMTczNDE4MTQxMTIzIiwKICAgICJwb3J0IjogNDQzLAogICAgInBzIjogIvCfh7rwn4e4VVMtNjcuMjEuNzIuNDEtOTg3OCIsCiAgICAidGxzIjogInRscyIsCiAgICAidHlwZSI6ICJhdXRvIiwKICAgICJzZWN1cml0eSI6ICJhdXRvIiwKICAgICJza2lwLWNlcnQtdmVyaWZ5IjogdHJ1ZSwKICAgICJzbmkiOiAiIgp9
    ss://YWVzLTI1Ni1jZmI6Yndoc2tyc2tyMDU=@97.64.122.63:253#%F0%9F%87%BA%F0%9F%87%B8US-97.64.122.63-15606
    vmess://ewogICAgImFkZCI6ICI2Ny4yMS43Mi40MSIsCiAgICAiYWlkIjogNjQsCiAgICAiaG9zdCI6ICIiLAogICAgImlkIjogIjI1NjZkMDBmLTIxOGMtNDhmNy05YTM2LTEzZDNkNmYxYTcyNCIsCiAgICAibmV0IjogIndzIiwKICAgICJwYXRoIjogIi9wYXRoLzE3MzQxODE0MTEyMyIsCiAgICAicG9ydCI6IDQ0MywKICAgICJwcyI6ICLwn4e68J+HuFVTLTY3LjIxLjcyLjQxLTQ4OTQiLAogICAgInRscyI6ICJ0bHMiLAogICAgInR5cGUiOiAiYXV0byIsCiAgICAic2VjdXJpdHkiOiAiYXV0byIsCiAgICAic2tpcC1jZXJ0LXZlcmlmeSI6IHRydWUsCiAgICAic25pIjogIiIKfQ==
    vmess://ewogICAgImFkZCI6ICJ2dXMyLjBiYWQuY29tIiwKICAgICJhaWQiOiAwLAogICAgImhvc3QiOiAidnVzMi4wYmFkLmNvbSIsCiAgICAiaWQiOiAiOTI3MDk0ZDMtZDY3OC00NzYzLTg1OTEtZTI0MGQwYmNhZTg3IiwKICAgICJuZXQiOiAid3MiLAogICAgInBhdGgiOiAiL2NoYXQiLAogICAgInBvcnQiOiA0NDMsCiAgICAicHMiOiAi8J+HuvCfh7hVUy00NS4zMy4xMDUuMjM5LTEwODE3IiwKICAgICJ0bHMiOiAidGxzIiwKICAgICJ0eXBlIjogImF1dG8iLAogICAgInNlY3VyaXR5IjogImF1dG8iLAogICAgInNraXAtY2VydC12ZXJpZnkiOiB0cnVlLAogICAgInNuaSI6ICIiCn0=
    vmess://ewogICAgImFkZCI6ICJ2dXMzLjBiYWQuY29tIiwKICAgICJhaWQiOiAwLAogICAgImhvc3QiOiAidnVzMy4wYmFkLmNvbSIsCiAgICAiaWQiOiAiOTI3MDk0ZDMtZDY3OC00NzYzLTg1OTEtZTI0MGQwYmNhZTg3IiwKICAgICJuZXQiOiAid3MiLAogICAgInBhdGgiOiAiL2NoYXQiLAogICAgInBvcnQiOiA0NDMsCiAgICAicHMiOiAi8J+HuvCfh7hVUy00NS43OS4yMjQuNTMtMTExNyIsCiAgICAidGxzIjogInRscyIsCiAgICAidHlwZSI6ICJhdXRvIiwKICAgICJzZWN1cml0eSI6ICJhdXRvIiwKICAgICJza2lwLWNlcnQtdmVyaWZ5IjogdHJ1ZSwKICAgICJzbmkiOiAiIgp9
    vmess://ewogICAgImFkZCI6ICI2Ny4yMS43Mi40NCIsCiAgICAiYWlkIjogNjQsCiAgICAiaG9zdCI6ICJ3d3cuNDg4MTY2MjYueHl6IiwKICAgICJpZCI6ICIyNTY2ZDAwZi0yMThjLTQ4ZjctOWEzNi0xM2QzZDZmMWE3MjQiLAogICAgIm5ldCI6ICJ3cyIsCiAgICAicGF0aCI6ICIvcGF0aC8xMjAyMDgzMDE0MjIiLAogICAgInBvcnQiOiA0NDMsCiAgICAicHMiOiAi8J+HuvCfh7hVUy02Ny4yMS43Mi40NC00ODkxIiwKICAgICJ0bHMiOiAidGxzIiwKICAgICJ0eXBlIjogImF1dG8iLAogICAgInNlY3VyaXR5IjogImF1dG8iLAogICAgInNraXAtY2VydC12ZXJpZnkiOiB0cnVlLAogICAgInNuaSI6ICIiCn0=
    ss://YWVzLTI1Ni1jZmI6Yndoc2tyc2tyMDU=@198.181.56.163:238#%F0%9F%87%BA%F0%9F%87%B8US-198.181.56.163-15629
    vmess://ewogICAgImFkZCI6ICI2Ny4yMS43Mi40NCIsCiAgICAiYWlkIjogNjQsCiAgICAiaG9zdCI6ICIiLAogICAgImlkIjogIjI1NjZkMDBmLTIxOGMtNDhmNy05YTM2LTEzZDNkNmYxYTcyNCIsCiAgICAibmV0IjogIndzIiwKICAgICJwYXRoIjogIi9wYXRoLzEyMDIwODMwMTQyMiIsCiAgICAicG9ydCI6IDQ0MywKICAgICJwcyI6ICLwn4e68J+HuFVTLTY3LjIxLjcyLjQ0LTEwMzA5IiwKICAgICJ0bHMiOiAidGxzIiwKICAgICJ0eXBlIjogImF1dG8iLAogICAgInNlY3VyaXR5IjogImF1dG8iLAogICAgInNraXAtY2VydC12ZXJpZnkiOiB0cnVlLAogICAgInNuaSI6ICIiCn0=
    vmess://ewogICAgImFkZCI6ICI2Ny4yMS43Mi40NCIsCiAgICAiYWlkIjogNjQsCiAgICAiaG9zdCI6ICI2Ny4yMS43Mi40NCIsCiAgICAiaWQiOiAiMjU2NmQwMGYtMjE4Yy00OGY3LTlhMzYtMTNkM2Q2ZjFhNzI0IiwKICAgICJuZXQiOiAid3MiLAogICAgInBhdGgiOiAiL3BhdGgvMTIwMjA4MzAxNDIyIiwKICAgICJwb3J0IjogNDQzLAogICAgInBzIjogIvCfh7rwn4e4VVMtNjcuMjEuNzIuNDQtMTAyODEiLAogICAgInRscyI6ICJ0bHMiLAogICAgInR5cGUiOiAiYXV0byIsCiAgICAic2VjdXJpdHkiOiAiYXV0byIsCiAgICAic2tpcC1jZXJ0LXZlcmlmeSI6IHRydWUsCiAgICAic25pIjogIiIKfQ==
    ss://YWVzLTEyOC1nY206c2hhZG93c29ja3M=@212.102.53.198:443#%F0%9F%87%AC%F0%9F%87%A7GB-212.102.53.198-0803
    ss://YWVzLTEyOC1nY206c2hhZG93c29ja3M=@212.102.53.79:443#%F0%9F%87%AC%F0%9F%87%A7GB-212.102.53.79-0800
    ss://YWVzLTEyOC1nY206c2hhZG93c29ja3M=@212.102.53.193:443#%F0%9F%87%AC%F0%9F%87%A7GB-212.102.53.193-0998
    ss://YWVzLTEyOC1nY206c2hhZG93c29ja3M=@212.102.53.81:443#%F0%9F%87%AC%F0%9F%87%A7GB-212.102.53.81-0561
    trojan://e23f408a-012e-4030-8b31-02022031cb50@fhcamd1.gaox.ml:443?allowInsecure=1#%F0%9F%87%BA%F0%9F%87%B8US-129.146.135.157-16738
    ss://YWVzLTEyOC1nY206c2hhZG93c29ja3M=@212.102.53.194:443#%F0%9F%87%AC%F0%9F%87%A7GB-212.102.53.194-0535
    ss://YWVzLTEyOC1nY206c2hhZG93c29ja3M=@212.102.53.195:443#%F0%9F%87%AC%F0%9F%87%A7GB-212.102.53.195-0802
    ss://YWVzLTEyOC1nY206c2hhZG93c29ja3M=@212.102.53.78:443#%F0%9F%87%AC%F0%9F%87%A7GB-212.102.53.78-0533
    ss://YWVzLTEyOC1nY206c2hhZG93c29ja3M=@212.102.53.196:443#%F0%9F%87%AC%F0%9F%87%A7GB-212.102.53.196-1355
    ss://YWVzLTEyOC1nY206c2hhZG93c29ja3M=@212.102.53.80:443#%F0%9F%87%AC%F0%9F%87%A7GB-212.102.53.80-0997
    ss://YWVzLTEyOC1nY206c2hhZG93c29ja3M=@212.102.53.197:443#%F0%9F%87%AC%F0%9F%87%A7GB-212.102.53.197-0562
    vmess://ewogICAgImFkZCI6ICIxMjkuMTU5LjQxLjIzMyIsCiAgICAiYWlkIjogMCwKICAgICJob3N0IjogIiIsCiAgICAiaWQiOiAiMzQxYTkxODItYzQyMy00OTljLWM0NmUtZDE3ODM4YjI5MDM3IiwKICAgICJuZXQiOiAidGNwIiwKICAgICJwYXRoIjogIiIsCiAgICAicG9ydCI6IDMyNTg2LAogICAgInBzIjogIvCfh7rwn4e4VVMtMTI5LjE1OS40MS4yMzMtMDIzOSIsCiAgICAidGxzIjogIiIsCiAgICAidHlwZSI6ICJhdXRvIiwKICAgICJzZWN1cml0eSI6ICJhdXRvIiwKICAgICJza2lwLWNlcnQtdmVyaWZ5IjogdHJ1ZSwKICAgICJzbmkiOiAiIgp9
    vmess://ewogICAgImFkZCI6ICIxMjkuMTQ2LjEzMy4xNTciLAogICAgImFpZCI6IDAsCiAgICAiaG9zdCI6ICIiLAogICAgImlkIjogIjgxNzE0Y2VmLTliZGUtNGEwOC1hYTUwLWQ2YmMwMTcyZDc4YiIsCiAgICAibmV0IjogInRjcCIsCiAgICAicGF0aCI6ICIiLAogICAgInBvcnQiOiA1MTAwOSwKICAgICJwcyI6ICLwn4e68J+HuFVTLTEyOS4xNDYuMTMzLjE1Ny0wMjc1IiwKICAgICJ0bHMiOiAiIiwKICAgICJ0eXBlIjogImF1dG8iLAogICAgInNlY3VyaXR5IjogImF1dG8iLAogICAgInNraXAtY2VydC12ZXJpZnkiOiB0cnVlLAogICAgInNuaSI6ICIiCn0=
    vmess://ewogICAgImFkZCI6ICIxNzIuNjQuMTU0LjE1MCIsCiAgICAiYWlkIjogMCwKICAgICJob3N0IjogImNsYXNoNi5zc3ItZnJlZS54eXoiLAogICAgImlkIjogIjVmNjRmYTY1LTdiMTQtNDljNS05NTRkLWFhMTVjNmJmY2FjZCIsCiAgICAibmV0IjogIndzIiwKICAgICJwYXRoIjogIi9kb25ndGFpd2FuZy5jb20iLAogICAgInBvcnQiOiA0NDMsCiAgICAicHMiOiAi8J+PgVJFTEFZLTE3Mi42NC4xNTQuMTUwLTAyNTEiLAogICAgInRscyI6ICJ0bHMiLAogICAgInR5cGUiOiAiYXV0byIsCiAgICAic2VjdXJpdHkiOiAiYXV0byIsCiAgICAic2tpcC1jZXJ0LXZlcmlmeSI6IHRydWUsCiAgICAic25pIjogIiIKfQ==
    ss://Y2hhY2hhMjAtaWV0Zi1wb2x5MTMwNTpHIXlCd1BXSDNWYW8=@78.129.253.9:808#%F0%9F%87%AC%F0%9F%87%A7GB-78.129.253.9-15647
    ss://Y2hhY2hhMjAtaWV0Zi1wb2x5MTMwNTpHIXlCd1BXSDNWYW8=@78.129.253.9:809#%F0%9F%87%AC%F0%9F%87%A7GB-78.129.253.9-1394
    ss://YWVzLTI1Ni1jZmI6Yndoc2tyc2tyMDE=@65.49.204.125:254#%F0%9F%87%BA%F0%9F%87%B8US-65.49.204.125-15627
    vmess://ewogICAgImFkZCI6ICJ2dWsyLjBiYWQuY29tIiwKICAgICJhaWQiOiAwLAogICAgImhvc3QiOiAidnVrMi4wYmFkLmNvbSIsCiAgICAiaWQiOiAiOTI3MDk0ZDMtZDY3OC00NzYzLTg1OTEtZTI0MGQwYmNhZTg3IiwKICAgICJuZXQiOiAid3MiLAogICAgInBhdGgiOiAiL2NoYXQiLAogICAgInBvcnQiOiA0NDMsCiAgICAicHMiOiAi8J+HrPCfh6dHQi0xMDkuNzQuMTk0LjIwOC0xMjQ5IiwKICAgICJ0bHMiOiAidGxzIiwKICAgICJ0eXBlIjogImF1dG8iLAogICAgInNlY3VyaXR5IjogImF1dG8iLAogICAgInNraXAtY2VydC12ZXJpZnkiOiB0cnVlLAogICAgInNuaSI6ICIiCn0=
    ss://Y2hhY2hhMjAtaWV0Zi1wb2x5MTMwNTpHIXlCd1BXSDNWYW8=@51.161.118.38:808#%F0%9F%87%A8%F0%9F%87%A6CA-51.161.118.38-15739
    vmess://ewogICAgImFkZCI6ICIxNzIuNjQuMTU1LjIwMSIsCiAgICAiYWlkIjogMCwKICAgICJob3N0IjogImNsYXNoMy50cnVtcDIwMjMub3JnIiwKICAgICJpZCI6ICIyOGRhZDY5Yy1jOWQ2LTQ3YzUtYWQwNS1jNjZhZmI4N2NjYmQiLAogICAgIm5ldCI6ICJ3cyIsCiAgICAicGF0aCI6ICIvZG9uZ3RhaXdhbmcuY29tIiwKICAgICJwb3J0IjogNDQzLAogICAgInBzIjogIvCfj4FSRUxBWS0xNzIuNjQuMTU1LjIwMS0wMjY2IiwKICAgICJ0bHMiOiAidGxzIiwKICAgICJ0eXBlIjogImF1dG8iLAogICAgInNlY3VyaXR5IjogImF1dG8iLAogICAgInNraXAtY2VydC12ZXJpZnkiOiB0cnVlLAogICAgInNuaSI6ICIiCn0=
    vmess://ewogICAgImFkZCI6ICIxOTguNDEuMjEyLjEwMCIsCiAgICAiYWlkIjogMCwKICAgICJob3N0IjogImZyMS5jZmNkbjEueHl6IiwKICAgICJpZCI6ICJmYjViYmM4Yy1mNmVjLTQ2MjktOGM5ZS0yM2YwMjc4MWEyMGQiLAogICAgIm5ldCI6ICJ3cyIsCiAgICAicGF0aCI6ICIvZG9uZ3RhaXdhbmcuY29tIiwKICAgICJwb3J0IjogNDQzLAogICAgInBzIjogIvCfj4FSRUxBWS0xOTguNDEuMjEyLjEwMC04NjEwIiwKICAgICJ0bHMiOiAidGxzIiwKICAgICJ0eXBlIjogImF1dG8iLAogICAgInNlY3VyaXR5IjogImF1dG8iLAogICAgInNraXAtY2VydC12ZXJpZnkiOiB0cnVlLAogICAgInNuaSI6ICIiCn0=
    ss://Y2hhY2hhMjAtaWV0Zi1wb2x5MTMwNTpHIXlCd1BXSDNWYW8=@51.161.118.38:800#%F0%9F%87%A8%F0%9F%87%A6CA-51.161.118.38-15732
    vmess://ewogICAgImFkZCI6ICJ2ZGUxLjBiYWQuY29tIiwKICAgICJhaWQiOiAwLAogICAgImhvc3QiOiAidmRlMS4wYmFkLmNvbSIsCiAgICAiaWQiOiAiOTI3MDk0ZDMtZDY3OC00NzYzLTg1OTEtZTI0MGQwYmNhZTg3IiwKICAgICJuZXQiOiAid3MiLAogICAgInBhdGgiOiAiL2NoYXQiLAogICAgInBvcnQiOiA0NDMsCiAgICAicHMiOiAi8J+HqfCfh6pERS0xNzIuMTA1LjI0NS43OS0wMjk4IiwKICAgICJ0bHMiOiAidGxzIiwKICAgICJ0eXBlIjogImF1dG8iLAogICAgInNlY3VyaXR5IjogImF1dG8iLAogICAgInNraXAtY2VydC12ZXJpZnkiOiB0cnVlLAogICAgInNuaSI6ICIiCn0=
    vmess://ewogICAgImFkZCI6ICJ2ZGUyLjBiYWQuY29tIiwKICAgICJhaWQiOiAwLAogICAgImhvc3QiOiAidmRlMi4wYmFkLmNvbSIsCiAgICAiaWQiOiAiOTI3MDk0ZDMtZDY3OC00NzYzLTg1OTEtZTI0MGQwYmNhZTg3IiwKICAgICJuZXQiOiAid3MiLAogICAgInBhdGgiOiAiL2NoYXQiLAogICAgInBvcnQiOiA0NDMsCiAgICAicHMiOiAi8J+HqfCfh6pERS0xMzkuMTQ0LjE3Ni43Ni0xMjgwIiwKICAgICJ0bHMiOiAidGxzIiwKICAgICJ0eXBlIjogImF1dG8iLAogICAgInNlY3VyaXR5IjogImF1dG8iLAogICAgInNraXAtY2VydC12ZXJpZnkiOiB0cnVlLAogICAgInNuaSI6ICIiCn0=
    ss://Y2hhY2hhMjAtaWV0Zi1wb2x5MTMwNTpHIXlCd1BXSDNWYW8=@134.195.196.178:804#%F0%9F%87%A8%F0%9F%87%A6CA-134.195.196.178-14790
    vmess://ewogICAgImFkZCI6ICJzdHJlYW0uYXphZHJhaDIyLmNvbSIsCiAgICAiYWlkIjogMCwKICAgICJob3N0IjogInN0cmVhbS5hemFkcmFoMjIuY29tIiwKICAgICJpZCI6ICI3NmUxNTFhNy05OTgwLTQwNzctYmQ1Mi0wN2VmNGU5Y2I0OTYiLAogICAgIm5ldCI6ICJ3cyIsCiAgICAicGF0aCI6ICIvdXNlciIsCiAgICAicG9ydCI6IDgwLAogICAgInBzIjogIvCfh67wn4e3SVItMTg1LjE0My4yMzQuMTIwLTE5NDk5IiwKICAgICJ0bHMiOiAiIiwKICAgICJ0eXBlIjogImF1dG8iLAogICAgInNlY3VyaXR5IjogImF1dG8iLAogICAgInNraXAtY2VydC12ZXJpZnkiOiB0cnVlLAogICAgInNuaSI6ICIiCn0=
    ss://Y2hhY2hhMjAtaWV0Zi1wb2x5MTMwNTpHIXlCd1BXSDNWYW8=@51.161.118.38:805#%F0%9F%87%A8%F0%9F%87%A6CA-51.161.118.38-15756
    ss://Y2hhY2hhMjAtaWV0Zi1wb2x5MTMwNTpHIXlCd1BXSDNWYW8=@51.161.118.38:806#%F0%9F%87%A8%F0%9F%87%A6CA-51.161.118.38-15744
    vmess://ewogICAgImFkZCI6ICJzdHVkeW5ldy5jbiIsCiAgICAiYWlkIjogMCwKICAgICJob3N0IjogInN0dWR5bmV3LmNuIiwKICAgICJpZCI6ICJiYjg0NzI1YS1mNzI2LTRiY2ItODEzMS00NGRmMTIwOTQwMDUiLAogICAgIm5ldCI6ICJ3cyIsCiAgICAicGF0aCI6ICIvZGVuZ3FpbmdibyIsCiAgICAicG9ydCI6IDUxMzQwLAogICAgInBzIjogIvCfh7rwn4e4VVMtMTk4LjE0OC4xMjcuNjItOTgxOSIsCiAgICAidGxzIjogInRscyIsCiAgICAidHlwZSI6ICJhdXRvIiwKICAgICJzZWN1cml0eSI6ICJhdXRvIiwKICAgICJza2lwLWNlcnQtdmVyaWZ5IjogdHJ1ZSwKICAgICJzbmkiOiAiIgp9
    vmess://ewogICAgImFkZCI6ICI4NS4xNy41LjE1MCIsCiAgICAiYWlkIjogMCwKICAgICJob3N0IjogIjg1LjE3LjUuMTUwIiwKICAgICJpZCI6ICI0MDcwZmRkZS00M2Q1LTRiM2YtZGJjZi03NzUxYzc3ZTRiZjYiLAogICAgIm5ldCI6ICJ3cyIsCiAgICAicGF0aCI6ICIvQWY1NjQ1dHIiLAogICAgInBvcnQiOiAzNjMwNiwKICAgICJwcyI6ICLwn4ez8J+HsU5MLTg1LjE3LjUuMTUwLTExNjE4IiwKICAgICJ0bHMiOiAiIiwKICAgICJ0eXBlIjogImF1dG8iLAogICAgInNlY3VyaXR5IjogImF1dG8iLAogICAgInNraXAtY2VydC12ZXJpZnkiOiB0cnVlLAogICAgInNuaSI6ICIiCn0=
    vmess://ewogICAgImFkZCI6ICI4NS4xNy41LjE1MCIsCiAgICAiYWlkIjogMCwKICAgICJob3N0IjogIiIsCiAgICAiaWQiOiAiNDA3MGZkZGUtNDNkNS00YjNmLWRiY2YtNzc1MWM3N2U0YmY2IiwKICAgICJuZXQiOiAid3MiLAogICAgInBhdGgiOiAiL0FmNTY0NXRyIiwKICAgICJwb3J0IjogMzYzMDYsCiAgICAicHMiOiAi8J+Hs/Cfh7FOTC04NS4xNy41LjE1MC0xMTYxMCIsCiAgICAidGxzIjogIiIsCiAgICAidHlwZSI6ICJhdXRvIiwKICAgICJzZWN1cml0eSI6ICJhdXRvIiwKICAgICJza2lwLWNlcnQtdmVyaWZ5IjogdHJ1ZSwKICAgICJzbmkiOiAiIgp9
    ss://Y2hhY2hhMjAtaWV0Zi1wb2x5MTMwNTpHIXlCd1BXSDNWYW8=@51.161.118.38:801#%F0%9F%87%A8%F0%9F%87%A6CA-51.161.118.38-15782
    ss://Y2hhY2hhMjAtaWV0Zi1wb2x5MTMwNTpHIXlCd1BXSDNWYW8=@162.251.61.221:807#%F0%9F%87%BA%F0%9F%87%B8US-162.251.61.221-0966
    ss://Y2hhY2hhMjAtaWV0Zi1wb2x5MTMwNTpHIXlCd1BXSDNWYW8=@162.251.61.221:811#%F0%9F%87%BA%F0%9F%87%B8US-162.251.61.221-2149
    ss://YWVzLTI1Ni1jZmI6ZjhmN2FDemNQS2JzRjhwMw==@194.71.126.31:989#%F0%9F%87%B7%F0%9F%87%B8RS-194.71.126.31-0408
    vmess://ewogICAgImFkZCI6ICIxNDEuMTAxLjExNS4xMjAiLAogICAgImFpZCI6IDAsCiAgICAiaG9zdCI6ICJsZzEuY2ZjZG4zLnh5eiIsCiAgICAiaWQiOiAiMzNhYTU3ZGYtMWM5My00MzE4LTlmY2UtZTg1MDQzN2VlNzgxIiwKICAgICJuZXQiOiAid3MiLAogICAgInBhdGgiOiAiL2Rvbmd0YWl3YW5nLmNvbSIsCiAgICAicG9ydCI6IDQ0MywKICAgICJwcyI6ICLwn4+BUkVMQVktMTQxLjEwMS4xMTUuMTIwLTEyMzQiLAogICAgInRscyI6ICJ0bHMiLAogICAgInR5cGUiOiAiYXV0byIsCiAgICAic2VjdXJpdHkiOiAiYXV0byIsCiAgICAic2tpcC1jZXJ0LXZlcmlmeSI6IHRydWUsCiAgICAic25pIjogIiIKfQ==
    trojan://8b6daf15-8342-482d-b894-1239fd98ce7f@149.56.141.11:443?allowInsecure=1#%F0%9F%87%A8%F0%9F%87%A6CA-149.56.141.11-0319
    ssr://NDUuMTU0LjIxNS4xMzU6MzE1ODA6YXV0aF9hZXMxMjhfc2hhMTphZXMtMjU2LWNmYjp0bHMxLjJfdGlja2V0X2F1dGg6ZW5oUGJXUkUvP29iZnNwYXJhbT1WbTB4TkdFd01VaFNXR2hVVjBkNFYxbHJaRk5XYkd4VlUycFNXRkp0ZUhwWGEyTTFZV3hLZEdWSWNGaGhNVlV4VmtkNFlXTXhXbkZXYkZaWFlsZG9VVmRXVm1GVGJWRjVWR3RXVW1KSGFGbFZha0YzJnJlbWFya3M9OEolMkJIdXZDZmg3aFZVeTAwTlM0eE5UUXVNakUxTGpFek5TMHlNemcxJnByb3RvcGFyYW09TWpJMk5qTTZVWEZNYjJGWg==
    vmess://ewogICAgImFkZCI6ICI1MS44OS40Mi4xNTQiLAogICAgImFpZCI6IDY0LAogICAgImhvc3QiOiAiIiwKICAgICJpZCI6ICI0MTgwNDhhZi1hMjkzLTRiOTktOWIwYy05OGNhMzU4MGRkMjQiLAogICAgIm5ldCI6ICJ3cyIsCiAgICAicGF0aCI6ICIvcGF0aC8xMjAyMTEzMzE0MjIiLAogICAgInBvcnQiOiA0NDMsCiAgICAicHMiOiAi8J+HrPCfh6dHQi01MS44OS40Mi4xNTQtMTY5ODkiLAogICAgInRscyI6ICJ0bHMiLAogICAgInR5cGUiOiAiYXV0byIsCiAgICAic2VjdXJpdHkiOiAiYXV0byIsCiAgICAic2tpcC1jZXJ0LXZlcmlmeSI6IHRydWUsCiAgICAic25pIjogIiIKfQ==
    trojan://8b6daf15-8342-482d-b894-1239fd98ce7f@cat1.sshocean.net:443?allowInsecure=1#%F0%9F%87%A8%F0%9F%87%A6CA-149.56.141.11-0241
    ss://Y2hhY2hhMjAtaWV0Zi1wb2x5MTMwNTo5N09uREVaWUdqYTQ=@178.18.244.2:443#%F0%9F%87%A9%F0%9F%87%AADE-178.18.244.2-0756
    ss://Y2hhY2hhMjAtaWV0Zi1wb2x5MTMwNTpzaUY5OHhCTDJ2MWk=@135.181.114.242:8478#%F0%9F%87%AB%F0%9F%87%AEFI-135.181.114.242-0798
    ss://YWVzLTI1Ni1jZmI6R2VyZWdldFI4Y3ZRSHpZcg==@213.183.53.221:9030#%F0%9F%87%B7%F0%9F%87%BARU-213.183.53.221-15695
    ss://YWVzLTI1Ni1jZmI6ZjhucEtnTnpka3NzMnl0bg==@213.183.53.221:9088#%F0%9F%87%B7%F0%9F%87%BARU-213.183.53.221-15694
    ss://Y2hhY2hhMjAtaWV0Zi1wb2x5MTMwNTopMU4xRTZ2MFNVX3JHVHBn@38.64.138.53:1035#%F0%9F%87%BA%F0%9F%87%B8US-38.64.138.53-0573
    ss://Y2hhY2hhMjAtaWV0Zi1wb2x5MTMwNTpHIXlCd1BXSDNWYW8=@162.251.61.47:805#%F0%9F%87%BA%F0%9F%87%B8US-162.251.61.47-0761
    ss://Y2hhY2hhMjAtaWV0Zi1wb2x5MTMwNTpHIXlCd1BXSDNWYW8=@51.161.118.38:812#%F0%9F%87%A8%F0%9F%87%A6CA-51.161.118.38-15779
    ss://Y2hhY2hhMjAtaWV0Zi1wb2x5MTMwNTpXYWN3ZXRDaWY=@217.12.223.190:444#%F0%9F%87%BA%F0%9F%87%A6UA-217.12.223.190-0790
    ss://Y2hhY2hhMjAtaWV0Zi1wb2x5MTMwNTpHIXlCd1BXSDNWYW8=@196.247.59.154:808#%F0%9F%87%A8%F0%9F%87%A6CA-196.247.59.154-13651
    ss://Y2hhY2hhMjAtaWV0Zi1wb2x5MTMwNTpHIXlCd1BXSDNWYW8=@5.188.0.151:800#%F0%9F%87%BA%F0%9F%87%B8US-5.188.0.151-15704
    ss://Y2hhY2hhMjAtaWV0Zi1wb2x5MTMwNTpHIXlCd1BXSDNWYW8=@ak1466.free.www.outline.network:811#%F0%9F%87%A8%F0%9F%87%A6CA-196.247.59.156-7643
    ss://Y2hhY2hhMjAtaWV0Zi1wb2x5MTMwNTpHIXlCd1BXSDNWYW8=@162.251.61.221:809#%F0%9F%87%BA%F0%9F%87%B8US-162.251.61.221-0566
    ssr://anAtYW00OC02LmVxbm9kZS5uZXQ6ODA4MTpvcmlnaW46YWVzLTI1Ni1jZmI6dGxzMS4yX3RpY2tldF9hdXRoOlpVRnZhMkpoUkU0Mi8/b2Jmc3BhcmFtPSZyZW1hcmtzPThKJTJCSHIlMkZDZmg3VktVQzAxTkM0Mk5DNDFOeTR6TkMwd05UYzQmcHJvdG9wYXJhbT0=
    ss://Y2hhY2hhMjAtaWV0Zi1wb2x5MTMwNTpHIXlCd1BXSDNWYW8=@196.247.59.154:805#%F0%9F%87%A8%F0%9F%87%A6CA-196.247.59.154-15687
    vmess://ewogICAgImFkZCI6ICI1MS44OS40Mi4xNTQiLAogICAgImFpZCI6IDY0LAogICAgImhvc3QiOiAiNTEuODkuNDIuMTU0IiwKICAgICJpZCI6ICI0MTgwNDhhZi1hMjkzLTRiOTktOWIwYy05OGNhMzU4MGRkMjQiLAogICAgIm5ldCI6ICJ3cyIsCiAgICAicGF0aCI6ICIvcGF0aC8xMjAyMTEzMzE0MjIiLAogICAgInBvcnQiOiA0NDMsCiAgICAicHMiOiAi8J+HrPCfh6dHQi01MS44OS40Mi4xNTQtMTEzNTciLAogICAgInRscyI6ICJ0bHMiLAogICAgInR5cGUiOiAiYXV0byIsCiAgICAic2VjdXJpdHkiOiAiYXV0byIsCiAgICAic2tpcC1jZXJ0LXZlcmlmeSI6IHRydWUsCiAgICAic25pIjogIiIKfQ==
    vmess://ewogICAgImFkZCI6ICIxNDEuMTAxLjExNS4yIiwKICAgICJhaWQiOiAwLAogICAgImhvc3QiOiAiZnIxLmNmY2RuMS54eXoiLAogICAgImlkIjogImZiNWJiYzhjLWY2ZWMtNDYyOS04YzllLTIzZjAyNzgxYTIwZCIsCiAgICAibmV0IjogIndzIiwKICAgICJwYXRoIjogIi9kb25ndGFpd2FuZy5jb20iLAogICAgInBvcnQiOiA0NDMsCiAgICAicHMiOiAi8J+PgVJFTEFZLTE0MS4xMDEuMTE1LjItMDI0NCIsCiAgICAidGxzIjogInRscyIsCiAgICAidHlwZSI6ICJhdXRvIiwKICAgICJzZWN1cml0eSI6ICJhdXRvIiwKICAgICJza2lwLWNlcnQtdmVyaWZ5IjogdHJ1ZSwKICAgICJzbmkiOiAiIgp9
    vmess://ewogICAgImFkZCI6ICIxNTAuMjMwLjE5OS4xNzciLAogICAgImFpZCI6IDAsCiAgICAiaG9zdCI6ICIiLAogICAgImlkIjogIjZiNzQ1Y2FmLWU3ZjYtNDlmMS05YjYzLWU1YzQxNjMwM2JhYyIsCiAgICAibmV0IjogInRjcCIsCiAgICAicGF0aCI6ICIiLAogICAgInBvcnQiOiAyMTY5NiwKICAgICJwcyI6ICLwn4ev8J+HtUpQLTE1MC4yMzAuMTk5LjE3Ny0wMjM3IiwKICAgICJ0bHMiOiAiIiwKICAgICJ0eXBlIjogImF1dG8iLAogICAgInNlY3VyaXR5IjogImF1dG8iLAogICAgInNraXAtY2VydC12ZXJpZnkiOiB0cnVlLAogICAgInNuaSI6ICIiCn0=
    vmess://ewogICAgImFkZCI6ICIxNDQuMjQuODguMTAxIiwKICAgICJhaWQiOiAwLAogICAgImhvc3QiOiAiIiwKICAgICJpZCI6ICJmNTQyNWNjZi0zOTQ2LTRmYjQtZWIyNC01MzkzZDc4YTM5MmYiLAogICAgIm5ldCI6ICJ0Y3AiLAogICAgInBhdGgiOiAiIiwKICAgICJwb3J0IjogMTY4MzMsCiAgICAicHMiOiAi8J+HsPCfh7dLUi0xNDQuMjQuODguMTAxLTA0NzYiLAogICAgInRscyI6ICIiLAogICAgInR5cGUiOiAiYXV0byIsCiAgICAic2VjdXJpdHkiOiAiYXV0byIsCiAgICAic2tpcC1jZXJ0LXZlcmlmeSI6IHRydWUsCiAgICAic25pIjogIiIKfQ==
    ss://Y2hhY2hhMjAtaWV0Zi1wb2x5MTMwNTpHIXlCd1BXSDNWYW8=@134.195.196.143:802#%F0%9F%87%A8%F0%9F%87%A6CA-134.195.196.143-15751
    vmess://ewogICAgImFkZCI6ICIxMzguMi4xNS4yMyIsCiAgICAiYWlkIjogMCwKICAgICJob3N0IjogIiIsCiAgICAiaWQiOiAiOTk4MTUxZTUtMGJjNS00Mzc3LWUzOTAtYzQxYmIyNmZkZDBjIiwKICAgICJuZXQiOiAidGNwIiwKICAgICJwYXRoIjogIiIsCiAgICAicG9ydCI6IDQ2MzcwLAogICAgInBzIjogIvCfh6/wn4e1SlAtMTM4LjIuMTUuMjMtMDI5MCIsCiAgICAidGxzIjogIiIsCiAgICAidHlwZSI6ICJhdXRvIiwKICAgICJzZWN1cml0eSI6ICJhdXRvIiwKICAgICJza2lwLWNlcnQtdmVyaWZ5IjogdHJ1ZSwKICAgICJzbmkiOiAiIgp9
    vmess://ewogICAgImFkZCI6ICJ2bTEyLmxlaWZlbmdrZWppLmxpdmUiLAogICAgImFpZCI6IDAsCiAgICAiaG9zdCI6ICJ2bTEyLmxlaWZlbmdrZWppLmxpdmUiLAogICAgImlkIjogIjc1MmE5NDA0LWM3MjktNDg1ZS04ZWE1LWFjYjNmNGZjODE4MCIsCiAgICAibmV0IjogIndzIiwKICAgICJwYXRoIjogIi8iLAogICAgInBvcnQiOiAxMTExMSwKICAgICJwcyI6ICLwn4ew8J+Ht0tSLTQzLjIwMS4zOC4xOTMtMTI5OSIsCiAgICAidGxzIjogIiIsCiAgICAidHlwZSI6ICJhdXRvIiwKICAgICJzZWN1cml0eSI6ICJhdXRvIiwKICAgICJza2lwLWNlcnQtdmVyaWZ5IjogdHJ1ZSwKICAgICJzbmkiOiAiIgp9
    vmess://ewogICAgImFkZCI6ICJ2bTUubGVpZmVuZ2tlamkubGl2ZSIsCiAgICAiYWlkIjogMCwKICAgICJob3N0IjogInZtNS5sZWlmZW5na2VqaS5saXZlIiwKICAgICJpZCI6ICI3NTJhOTQwNC1jNzI5LTQ4NWUtOGVhNS1hY2IzZjRmYzgxODAiLAogICAgIm5ldCI6ICJ3cyIsCiAgICAicGF0aCI6ICIvIiwKICAgICJwb3J0IjogMTExMTEsCiAgICAicHMiOiAi8J+HsPCfh7dLUi0xMy4yMDkuNC4yMTEtMDIyOCIsCiAgICAidGxzIjogIiIsCiAgICAidHlwZSI6ICJhdXRvIiwKICAgICJzZWN1cml0eSI6ICJhdXRvIiwKICAgICJza2lwLWNlcnQtdmVyaWZ5IjogdHJ1ZSwKICAgICJzbmkiOiAiIgp9
    trojan://752a9404-c729-485e-8ea5-acb3f4fc8180@hg5.leifengkeji.live:48903?allowInsecure=1#%F0%9F%87%B0%F0%9F%87%B7KR-43.200.4.201-11721
    vmess://ewogICAgImFkZCI6ICIxNTIuNzAuMjQxLjE4IiwKICAgICJhaWQiOiAwLAogICAgImhvc3QiOiAiIiwKICAgICJpZCI6ICJlY2QyNzRjMC0xNzVkLTQ1ZjctODI3Ni1hM2RhOTM3ODY2MzIiLAogICAgIm5ldCI6ICJ0Y3AiLAogICAgInBhdGgiOiAiIiwKICAgICJwb3J0IjogMjY2NzYsCiAgICAicHMiOiAi8J+HsPCfh7dLUi0xNTIuNzAuMjQxLjE4LTAzMjgiLAogICAgInRscyI6ICIiLAogICAgInR5cGUiOiAiYXV0byIsCiAgICAic2VjdXJpdHkiOiAiYXV0byIsCiAgICAic2tpcC1jZXJ0LXZlcmlmeSI6IHRydWUsCiAgICAic25pIjogIiIKfQ==
    vmess://ewogICAgImFkZCI6ICIxOTIuNzQuMjQyLjE4MiIsCiAgICAiYWlkIjogNjQsCiAgICAiaG9zdCI6ICIiLAogICAgImlkIjogIjQxODA0OGFmLWEyOTMtNGI5OS05YjBjLTk4Y2EzNTgwZGQyNCIsCiAgICAibmV0IjogIndzIiwKICAgICJwYXRoIjogIi9wYXRoLzE3MDQxOTExMTAyMSIsCiAgICAicG9ydCI6IDQ0MywKICAgICJwcyI6ICLwn4e68J+HuFVTLTE5Mi43NC4yNDIuMTgyLTE2NjgzIiwKICAgICJ0bHMiOiAidGxzIiwKICAgICJ0eXBlIjogImF1dG8iLAogICAgInNlY3VyaXR5IjogImF1dG8iLAogICAgInNraXAtY2VydC12ZXJpZnkiOiB0cnVlLAogICAgInNuaSI6ICJ3d3cuMzIzMzgwNzUueHl6Igp9
    vmess://ewogICAgImFkZCI6ICJ2bTgubGVpZmVuZ2tlamkubGl2ZSIsCiAgICAiYWlkIjogMCwKICAgICJob3N0IjogInZtOC5sZWlmZW5na2VqaS5saXZlIiwKICAgICJpZCI6ICI3NTJhOTQwNC1jNzI5LTQ4NWUtOGVhNS1hY2IzZjRmYzgxODAiLAogICAgIm5ldCI6ICJ3cyIsCiAgICAicGF0aCI6ICIvIiwKICAgICJwb3J0IjogMTExMTEsCiAgICAicHMiOiAi8J+HsPCfh7dLUi0xNS4xNjQuMTYzLjE0LTExODg0IiwKICAgICJ0bHMiOiAiIiwKICAgICJ0eXBlIjogImF1dG8iLAogICAgInNlY3VyaXR5IjogImF1dG8iLAogICAgInNraXAtY2VydC12ZXJpZnkiOiB0cnVlLAogICAgInNuaSI6ICIiCn0=
    trojan://752a9404-c729-485e-8ea5-acb3f4fc8180@hg17.leifengkeji.live:33387?allowInsecure=1&sni=hg17.leifengkeji.live#%F0%9F%87%B0%F0%9F%87%B7KR-15.164.103.48-0255
    ss://Y2hhY2hhMjAtaWV0Zi1wb2x5MTMwNTpHIXlCd1BXSDNWYW8=@162.251.61.221:803#%F0%9F%87%BA%F0%9F%87%B8US-162.251.61.221-0571
    ss://Y2hhY2hhMjAtaWV0Zi1wb2x5MTMwNTpHIXlCd1BXSDNWYW8=@134.195.196.143:805#%F0%9F%87%A8%F0%9F%87%A6CA-134.195.196.143-15766
    vmess://ewogICAgImFkZCI6ICIxNDYuNTYuMTU1LjcwIiwKICAgICJhaWQiOiAwLAogICAgImhvc3QiOiAiIiwKICAgICJpZCI6ICJmOTc3MWMxOS1jOTFjLTQxYjUtOTA2NC04NzY4YjUxY2VjNmQiLAogICAgIm5ldCI6ICJ0Y3AiLAogICAgInBhdGgiOiAiIiwKICAgICJwb3J0IjogMTgwNTAsCiAgICAicHMiOiAi8J+HsPCfh7dLUi0xNDYuNTYuMTU1LjcwLTAzMjUiLAogICAgInRscyI6ICIiLAogICAgInR5cGUiOiAiYXV0byIsCiAgICAic2VjdXJpdHkiOiAiYXV0byIsCiAgICAic2tpcC1jZXJ0LXZlcmlmeSI6IHRydWUsCiAgICAic25pIjogIiIKfQ==
    ss://Y2hhY2hhMjAtaWV0Zi1wb2x5MTMwNTpHIXlCd1BXSDNWYW8=@196.247.59.154:801#%F0%9F%87%A8%F0%9F%87%A6CA-196.247.59.154-15760
    ss://Y2hhY2hhMjAtaWV0Zi1wb2x5MTMwNTpHIXlCd1BXSDNWYW8=@196.247.59.154:803#%F0%9F%87%A8%F0%9F%87%A6CA-196.247.59.154-15754
    ss://Y2hhY2hhMjAtaWV0Zi1wb2x5MTMwNTpHIXlCd1BXSDNWYW8=@162.251.61.221:802#%F0%9F%87%BA%F0%9F%87%B8US-162.251.61.221-0537
    trojan://0Y9gOHSdRt@150.230.249.42:443?allowInsecure=1#%F0%9F%87%B0%F0%9F%87%B7KR-150.230.249.42-0291
    ss://Y2hhY2hhMjAtaWV0Zi1wb2x5MTMwNTpHIXlCd1BXSDNWYW8=@37.120.147.230:805#%F0%9F%87%BA%F0%9F%87%B8US-37.120.147.230-0771
    ss://Y2hhY2hhMjAtaWV0Zi1wb2x5MTMwNTpHIXlCd1BXSDNWYW8=@196.247.59.154:800#%F0%9F%87%A8%F0%9F%87%A6CA-196.247.59.154-15677
    ss://Y2hhY2hhMjAtaWV0Zi1wb2x5MTMwNTpHIXlCd1BXSDNWYW8=@162.251.61.221:806#%F0%9F%87%BA%F0%9F%87%B8US-162.251.61.221-0553
    vmess://ewogICAgImFkZCI6ICIxNTIuNjcuMjE4LjM4IiwKICAgICJhaWQiOiAwLAogICAgImhvc3QiOiAiWW91VHViZS1hd2Vpa2VqaSIsCiAgICAiaWQiOiAiYjVlOTQ4MGEtYjdhYS00MGE0LWY5YTctNTI5OWI1ZTM2M2I0IiwKICAgICJuZXQiOiAid3MiLAogICAgInBhdGgiOiAiLyIsCiAgICAicG9ydCI6IDQ0MywKICAgICJwcyI6ICLwn4ew8J+Ht0tSLTE1Mi42Ny4yMTguMzgtMTU1NDUiLAogICAgInRscyI6ICIiLAogICAgInR5cGUiOiAiYXV0byIsCiAgICAic2VjdXJpdHkiOiAiYXV0byIsCiAgICAic2tpcC1jZXJ0LXZlcmlmeSI6IHRydWUsCiAgICAic25pIjogIiIKfQ==
    ss://Y2hhY2hhMjAtaWV0Zi1wb2x5MTMwNTpHIXlCd1BXSDNWYW8=@162.251.61.221:800#%F0%9F%87%BA%F0%9F%87%B8US-162.251.61.221-0543
    vmess://ewogICAgImFkZCI6ICI4LjIwOS4yMTguMTk1IiwKICAgICJhaWQiOiAwLAogICAgImhvc3QiOiAibGluZG8uY25hYmMuZXUub3JnIiwKICAgICJpZCI6ICJmNmQ3YjA3Mi1kZTAwLTQ1ZGMtOWUyNC00OWY4Y2Y0MzUzMGQiLAogICAgIm5ldCI6ICJ3cyIsCiAgICAicGF0aCI6ICIvbGlub2QiLAogICAgInBvcnQiOiA0NDMsCiAgICAicHMiOiAi8J+Hr/Cfh7VKUC04LjIwOS4yMTguMTk1LTAzMjYiLAogICAgInRscyI6ICJ0bHMiLAogICAgInR5cGUiOiAiYXV0byIsCiAgICAic2VjdXJpdHkiOiAiYXV0byIsCiAgICAic2tpcC1jZXJ0LXZlcmlmeSI6IHRydWUsCiAgICAic25pIjogIiIKfQ==
    vmess://ewogICAgImFkZCI6ICJ2bTE1LmxlaWZlbmdrZWppLmxpdmUiLAogICAgImFpZCI6IDAsCiAgICAiaG9zdCI6ICJ2bTE1LmxlaWZlbmdrZWppLmxpdmUiLAogICAgImlkIjogIjc1MmE5NDA0LWM3MjktNDg1ZS04ZWE1LWFjYjNmNGZjODE4MCIsCiAgICAibmV0IjogIndzIiwKICAgICJwYXRoIjogIi8iLAogICAgInBvcnQiOiAxMTExMSwKICAgICJwcyI6ICLwn4ew8J+Ht0tSLTU0LjE4MC4xMDEuNi0wMjkzIiwKICAgICJ0bHMiOiAiIiwKICAgICJ0eXBlIjogImF1dG8iLAogICAgInNlY3VyaXR5IjogImF1dG8iLAogICAgInNraXAtY2VydC12ZXJpZnkiOiB0cnVlLAogICAgInNuaSI6ICIiCn0=
    vmess://ewogICAgImFkZCI6ICJhZWFkanBhZXMwMS54bi0tejRxNDhsY3ZwLmNvbSIsCiAgICAiYWlkIjogMCwKICAgICJob3N0IjogInNob3V0aW5ndG91dGlhbzMuMTAwMTAuY29tIiwKICAgICJpZCI6ICIzZTgyMGViMC0zZjA2LTQzMzctYTRmYy0wYzNjN2MwZDNiNGQiLAogICAgIm5ldCI6ICJ3cyIsCiAgICAicGF0aCI6ICIvaW1hZ2VzIiwKICAgICJwb3J0IjogODAsCiAgICAicHMiOiAi8J+Hr/Cfh7VKUC0xNzIuMTA0Ljc5Ljk2LTE2MTA3IiwKICAgICJ0bHMiOiAiIiwKICAgICJ0eXBlIjogImF1dG8iLAogICAgInNlY3VyaXR5IjogImF1dG8iLAogICAgInNraXAtY2VydC12ZXJpZnkiOiB0cnVlLAogICAgInNuaSI6ICIiCn0=
    vmess://ewogICAgImFkZCI6ICIxNTIuNjcuMjE4LjM4IiwKICAgICJhaWQiOiAwLAogICAgImhvc3QiOiAiMTUyLjY3LjIxOC4zOCIsCiAgICAiaWQiOiAiYjVlOTQ4MGEtYjdhYS00MGE0LWY5YTctNTI5OWI1ZTM2M2I0IiwKICAgICJuZXQiOiAid3MiLAogICAgInBhdGgiOiAiLyIsCiAgICAicG9ydCI6IDQ0MywKICAgICJwcyI6ICLwn4ew8J+Ht0tSLTE1Mi42Ny4yMTguMzgtMDIyNCIsCiAgICAidGxzIjogIiIsCiAgICAidHlwZSI6ICJhdXRvIiwKICAgICJzZWN1cml0eSI6ICJhdXRvIiwKICAgICJza2lwLWNlcnQtdmVyaWZ5IjogdHJ1ZSwKICAgICJzbmkiOiAiIgp9
    vmess://ewogICAgImFkZCI6ICIxMjkuMTU0LjU3LjEzNCIsCiAgICAiYWlkIjogMCwKICAgICJob3N0IjogIiIsCiAgICAiaWQiOiAiY2FiYmRmNWQtM2NjYS00NjA1LWJhMWMtYzg5YTdkNWI0YzA3IiwKICAgICJuZXQiOiAidGNwIiwKICAgICJwYXRoIjogIiIsCiAgICAicG9ydCI6IDI2MjgyLAogICAgInBzIjogIvCfh7Dwn4e3S1ItMTI5LjE1NC41Ny4xMzQtMDMyMyIsCiAgICAidGxzIjogIiIsCiAgICAidHlwZSI6ICJhdXRvIiwKICAgICJzZWN1cml0eSI6ICJhdXRvIiwKICAgICJza2lwLWNlcnQtdmVyaWZ5IjogdHJ1ZSwKICAgICJzbmkiOiAiIgp9
    ss://Y2hhY2hhMjAtaWV0Zi1wb2x5MTMwNTp2QXBZaUFnaHplc0g=@217.70.188.60:855#%F0%9F%87%AB%F0%9F%87%B7FR-217.70.188.60-15709
    vmess://ewogICAgImFkZCI6ICI1MS44OS40Mi4xNTQiLAogICAgImFpZCI6IDY0LAogICAgImhvc3QiOiAiIiwKICAgICJpZCI6ICI0MTgwNDhhZi1hMjkzLTRiOTktOWIwYy05OGNhMzU4MGRkMjQiLAogICAgIm5ldCI6ICJ3cyIsCiAgICAicGF0aCI6ICIvcGF0aC8xMjAyMTEzMzE0MjIiLAogICAgInBvcnQiOiA0NDMsCiAgICAicHMiOiAi8J+HrPCfh6dHQi01MS44OS40Mi4xNTQtMjM3OSIsCiAgICAidGxzIjogInRscyIsCiAgICAidHlwZSI6ICJhdXRvIiwKICAgICJzZWN1cml0eSI6ICJhdXRvIiwKICAgICJza2lwLWNlcnQtdmVyaWZ5IjogdHJ1ZSwKICAgICJzbmkiOiAiIgp9
    vmess://ewogICAgImFkZCI6ICJtNC40MDAxMDAxMC54eXoiLAogICAgImFpZCI6IDAsCiAgICAiaG9zdCI6ICIiLAogICAgImlkIjogIjU3NWU0ZDkyLTEwNTYtNDRjMi04Y2FjLTc1ZWYxYzg1OWFkNSIsCiAgICAibmV0IjogInRjcCIsCiAgICAicGF0aCI6ICIiLAogICAgInBvcnQiOiAzNzEyMSwKICAgICJwcyI6ICLwn4ew8J+Ht0tSLTE0Ni41Ni4xMzMuMTA5LTAyODUiLAogICAgInRscyI6ICJ0bHMiLAogICAgInR5cGUiOiAiYXV0byIsCiAgICAic2VjdXJpdHkiOiAiYXV0byIsCiAgICAic2tpcC1jZXJ0LXZlcmlmeSI6IHRydWUsCiAgICAic25pIjogIiIKfQ==
    ss://Y2hhY2hhMjAtaWV0Zi1wb2x5MTMwNTpHIXlCd1BXSDNWYW8=@37.120.147.230:800#%F0%9F%87%BA%F0%9F%87%B8US-37.120.147.230-10336
    vmess://ewogICAgImFkZCI6ICJ3d3cuYXB1bG5pb24uY29tIiwKICAgICJhaWQiOiAwLAogICAgImhvc3QiOiAid3d3LmFwdWxuaW9uLmNvbSIsCiAgICAiaWQiOiAiN2I4YzM3MGQtODYxMC00OTg4LWIwYTctY2RlNzRhYTA3MTNiIiwKICAgICJuZXQiOiAid3MiLAogICAgInBhdGgiOiAiLzU4YTUzNDJmN2EvIiwKICAgICJwb3J0IjogNDQzLAogICAgInBzIjogIvCfh7Dwn4e3S1ItMTMyLjIyNi4xNzMuMTE4LTAzMzEiLAogICAgInRscyI6ICJ0bHMiLAogICAgInR5cGUiOiAiYXV0byIsCiAgICAic2VjdXJpdHkiOiAiYXV0byIsCiAgICAic2tpcC1jZXJ0LXZlcmlmeSI6IHRydWUsCiAgICAic25pIjogIiIKfQ==
    vmess://ewogICAgImFkZCI6ICIxNTIuNzAuMjM1LjIwNyIsCiAgICAiYWlkIjogMCwKICAgICJob3N0IjogIiIsCiAgICAiaWQiOiAiNzBkOTUzMDgtMmE2MS00ZjkzLWYxMzktOTEwM2QwNTg3ZmQ5IiwKICAgICJuZXQiOiAidGNwIiwKICAgICJwYXRoIjogIiIsCiAgICAicG9ydCI6IDM1NDEyLAogICAgInBzIjogIvCfh7Dwn4e3S1ItMTUyLjcwLjIzNS4yMDctMDI3MSIsCiAgICAidGxzIjogIiIsCiAgICAidHlwZSI6ICJhdXRvIiwKICAgICJzZWN1cml0eSI6ICJhdXRvIiwKICAgICJza2lwLWNlcnQtdmVyaWZ5IjogdHJ1ZSwKICAgICJzbmkiOiAiIgp9
    vmess://ewogICAgImFkZCI6ICIxOC4xNDMuMTIzLjM1IiwKICAgICJhaWQiOiAwLAogICAgImhvc3QiOiAiZG0udG91dGlhby5jb20iLAogICAgImlkIjogIjY4ZGY0ODM4LTQ2ZDAtNGI1Yi1jM2YwLWE0MGVjNzA2MzI0NSIsCiAgICAibmV0IjogIndzIiwKICAgICJwYXRoIjogIi8iLAogICAgInBvcnQiOiA4MCwKICAgICJwcyI6ICLwn4e48J+HrFNHLTE4LjE0My4xMjMuMzUtMTU3MzMiLAogICAgInRscyI6ICIiLAogICAgInR5cGUiOiAiYXV0byIsCiAgICAic2VjdXJpdHkiOiAiYXV0byIsCiAgICAic2tpcC1jZXJ0LXZlcmlmeSI6IHRydWUsCiAgICAic25pIjogIiIKfQ==
    ss://Y2hhY2hhMjAtaWV0Zi1wb2x5MTMwNTpHIXlCd1BXSDNWYW8=@162.251.61.221:804#%F0%9F%87%BA%F0%9F%87%B8US-162.251.61.221-0555
    vmess://ewogICAgImFkZCI6ICIxOC4xNDMuMTIzLjM1IiwKICAgICJhaWQiOiAwLAogICAgImhvc3QiOiAiIiwKICAgICJpZCI6ICI2OGRmNDgzOC00NmQwLTRiNWItYzNmMC1hNDBlYzcwNjMyNDUiLAogICAgIm5ldCI6ICJ3cyIsCiAgICAicGF0aCI6ICIvIiwKICAgICJwb3J0IjogODAsCiAgICAicHMiOiAi8J+HuPCfh6xTRy0xOC4xNDMuMTIzLjM1LTAzMzciLAogICAgInRscyI6ICIiLAogICAgInR5cGUiOiAiYXV0byIsCiAgICAic2VjdXJpdHkiOiAiYXV0byIsCiAgICAic2tpcC1jZXJ0LXZlcmlmeSI6IHRydWUsCiAgICAic25pIjogIiIKfQ==
    trojan://bb5b1337-fa9e-4e00-b8c6-1110e626171d@159.223.89.239:443?allowInsecure=1#%F0%9F%87%B8%F0%9F%87%ACSG-159.223.89.239-0240
    vmess://ewogICAgImFkZCI6ICIxOC4xNDMuMTIzLjM1IiwKICAgICJhaWQiOiAwLAogICAgImhvc3QiOiAiMTguMTQzLjEyMy4zNSIsCiAgICAiaWQiOiAiNjhkZjQ4MzgtNDZkMC00YjViLWMzZjAtYTQwZWM3MDYzMjQ1IiwKICAgICJuZXQiOiAid3MiLAogICAgInBhdGgiOiAiLyIsCiAgICAicG9ydCI6IDgwLAogICAgInBzIjogIvCfh7jwn4esU0ctMTguMTQzLjEyMy4zNS0xNTcyMCIsCiAgICAidGxzIjogIiIsCiAgICAidHlwZSI6ICJhdXRvIiwKICAgICJzZWN1cml0eSI6ICJhdXRvIiwKICAgICJza2lwLWNlcnQtdmVyaWZ5IjogdHJ1ZSwKICAgICJzbmkiOiAiIgp9
    trojan://bb5b1337-fa9e-4e00-b8c6-1110e626171d@sg-01.tiktokcdn.top:443?allowInsecure=1#%F0%9F%87%B8%F0%9F%87%ACSG-159.223.89.239-0282
    vmess://ewogICAgImFkZCI6ICIxMzguMi40NC4yMTEiLAogICAgImFpZCI6IDAsCiAgICAiaG9zdCI6ICIiLAogICAgImlkIjogIjU5M2I4NTI1LTBjNDgtNGIwZi1kOWFmLTJkNzNhOTE0ODk3MyIsCiAgICAibmV0IjogInRjcCIsCiAgICAicGF0aCI6ICIiLAogICAgInBvcnQiOiAyMDA4MSwKICAgICJwcyI6ICLwn4ev8J+HtUpQLTEzOC4yLjQ0LjIxMS0wMjYzIiwKICAgICJ0bHMiOiAiIiwKICAgICJ0eXBlIjogImF1dG8iLAogICAgInNlY3VyaXR5IjogImF1dG8iLAogICAgInNraXAtY2VydC12ZXJpZnkiOiB0cnVlLAogICAgInNuaSI6ICIiCn0=
    vmess://ewogICAgImFkZCI6ICIxNTIuNjkuMTk3LjYwIiwKICAgICJhaWQiOiAwLAogICAgImhvc3QiOiAiIiwKICAgICJpZCI6ICJhYzhlMjZmZS04MTUwLTRiNjAtYWU2NC04MmZjNzdlYmEyY2YiLAogICAgIm5ldCI6ICJ0Y3AiLAogICAgInBhdGgiOiAiIiwKICAgICJwb3J0IjogMTA2OSwKICAgICJwcyI6ICLwn4ev8J+HtUpQLTE1Mi42OS4xOTcuNjAtMTM5OSIsCiAgICAidGxzIjogIiIsCiAgICAidHlwZSI6ICJhdXRvIiwKICAgICJzZWN1cml0eSI6ICJhdXRvIiwKICAgICJza2lwLWNlcnQtdmVyaWZ5IjogdHJ1ZSwKICAgICJzbmkiOiAiIgp9
    vmess://ewogICAgImFkZCI6ICIxNjcuMTcyLjY0LjExIiwKICAgICJhaWQiOiAwLAogICAgImhvc3QiOiAiIiwKICAgICJpZCI6ICI3NmEyNzZhMi0wZmMzLTRiZmItY2IwMC02Y2QyYTQzMDk2NzciLAogICAgIm5ldCI6ICJ0Y3AiLAogICAgInBhdGgiOiAiIiwKICAgICJwb3J0IjogMTAwODYsCiAgICAicHMiOiAi8J+HuPCfh6xTRy0xNjcuMTcyLjY0LjExLTAyMzQiLAogICAgInRscyI6ICIiLAogICAgInR5cGUiOiAiYXV0byIsCiAgICAic2VjdXJpdHkiOiAiYXV0byIsCiAgICAic2tpcC1jZXJ0LXZlcmlmeSI6IHRydWUsCiAgICAic25pIjogIiIKfQ==
    vmess://ewogICAgImFkZCI6ICIxNTIuNjkuMTk3LjYwIiwKICAgICJhaWQiOiAwLAogICAgImhvc3QiOiAiIiwKICAgICJpZCI6ICJhYzhlMjZmZS04MTUwLTRiNjAtYWU2NC04MmZjNzdlYmEyY2YiLAogICAgIm5ldCI6ICJ0Y3AiLAogICAgInBhdGgiOiAiIiwKICAgICJwb3J0IjogMTA2OSwKICAgICJwcyI6ICLwn4ev8J+HtUpQLTE1Mi42OS4xOTcuNjAtMDMyMCIsCiAgICAidGxzIjogIiIsCiAgICAidHlwZSI6ICJhdXRvIiwKICAgICJzZWN1cml0eSI6ICJhdXRvIiwKICAgICJza2lwLWNlcnQtdmVyaWZ5IjogdHJ1ZSwKICAgICJzbmkiOiAiIgp9
    vmess://ewogICAgImFkZCI6ICJzZzIwMi5oa2FhMC50ayIsCiAgICAiYWlkIjogMCwKICAgICJob3N0IjogInNnMjAyLmhrYWEwLnRrIiwKICAgICJpZCI6ICJiZGY3OThmNC1hOTkwLTQ3NDMtZTliMi05Yzc4YmE1OGZiMDQiLAogICAgIm5ldCI6ICJ3cyIsCiAgICAicGF0aCI6ICIvaGthYTAiLAogICAgInBvcnQiOiAxMDE4LAogICAgInBzIjogIvCfh7jwn4esU0ctMTcyLjEwNC4xNjMuMjAyLTE3MDg3IiwKICAgICJ0bHMiOiAiIiwKICAgICJ0eXBlIjogImF1dG8iLAogICAgInNlY3VyaXR5IjogImF1dG8iLAogICAgInNraXAtY2VydC12ZXJpZnkiOiB0cnVlLAogICAgInNuaSI6ICJzZzIwMi5oa2FhMC50ayIKfQ==
    ss://Y2hhY2hhMjAtaWV0Zi1wb2x5MTMwNTpHIXlCd1BXSDNWYW8=@37.120.219.218:809#%F0%9F%87%BA%F0%9F%87%B8US-37.120.219.218-15659
    ss://YWVzLTI1Ni1jZmI6dkRTOUcycA==@185.4.65.6:21247#%F0%9F%87%B7%F0%9F%87%BARU-185.4.65.6-15714
    ss://Y2hhY2hhMjAtaWV0Zi1wb2x5MTMwNTpHIXlCd1BXSDNWYW8=@37.120.219.218:803#%F0%9F%87%BA%F0%9F%87%B8US-37.120.219.218-15657
    trojan://cb43b7c2-b744-41c5-bcc2-fd7467b332cf@jgwxn3.gaox.ml:443?allowInsecure=1#%F0%9F%87%A6%F0%9F%87%BAAU-140.238.205.173-14885
    ss://Y2hhY2hhMjAtaWV0Zi1wb2x5MTMwNTpHIXlCd1BXSDNWYW8=@162.251.61.221:805#%F0%9F%87%BA%F0%9F%87%B8US-162.251.61.221-0538
    ss://Y2hhY2hhMjAtaWV0Zi1wb2x5MTMwNTpHIXlCd1BXSDNWYW8=@196.247.59.156:809#%F0%9F%87%A8%F0%9F%87%A6CA-196.247.59.156-15778
    trojan://c19d1432-8b3e-4818-8837-3d160cf65908@138.2.45.243:443?allowInsecure=1#%F0%9F%87%AF%F0%9F%87%B5JP-138.2.45.243-19249
    ss://Y2hhY2hhMjAtaWV0Zi1wb2x5MTMwNTpHIXlCd1BXSDNWYW8=@37.120.147.230:809#%F0%9F%87%BA%F0%9F%87%B8US-37.120.147.230-10334
    ss://Y2hhY2hhMjAtaWV0Zi1wb2x5MTMwNTpHIXlCd1BXSDNWYW8=@37.120.219.218:804#%F0%9F%87%BA%F0%9F%87%B8US-37.120.219.218-15656
    ss://Y2hhY2hhMjAtaWV0Zi1wb2x5MTMwNTpHIXlCd1BXSDNWYW8=@196.247.59.154:802#%F0%9F%87%A8%F0%9F%87%A6CA-196.247.59.154-15689
    ss://Y2hhY2hhMjAtaWV0Zi1wb2x5MTMwNTpHIXlCd1BXSDNWYW8=@38.91.107.225:805#%F0%9F%87%BA%F0%9F%87%B8US-38.91.107.225-15679
    vmess://ewogICAgImFkZCI6ICIxNzIuNjQuMTUzLjEwMiIsCiAgICAiYWlkIjogMCwKICAgICJob3N0IjogImNsYXNoMi50cnVtcDIwMjMudXMiLAogICAgImlkIjogImJlZDNkODc2LTJkMjYtNGQ0ZC1iNzg5LTMwNjM0MzhlZTc3NCIsCiAgICAibmV0IjogIndzIiwKICAgICJwYXRoIjogIi9kb25ndGFpd2FuZy5jb20iLAogICAgInBvcnQiOiA0NDMsCiAgICAicHMiOiAi8J+PgVJFTEFZLTE3Mi42NC4xNTMuMTAyLTEwNTQiLAogICAgInRscyI6ICJ0bHMiLAogICAgInR5cGUiOiAiYXV0byIsCiAgICAic2VjdXJpdHkiOiAiYXV0byIsCiAgICAic2tpcC1jZXJ0LXZlcmlmeSI6IHRydWUsCiAgICAic25pIjogIiIKfQ==
    ss://Y2hhY2hhMjAtaWV0Zi1wb2x5MTMwNTpHIXlCd1BXSDNWYW8=@38.91.107.225:809#%F0%9F%87%BA%F0%9F%87%B8US-38.91.107.225-15688
    vmess://ewogICAgImFkZCI6ICIxNi4xNjIuNTUuMTMwIiwKICAgICJhaWQiOiAwLAogICAgImhvc3QiOiAiMTYuMTYyLjU1LjEzMCIsCiAgICAiaWQiOiAiMTliOTVhMGUtZmZjZi0zMmVkLTg2NTYtNTJhZTEwMmE4YWQ4IiwKICAgICJuZXQiOiAid3MiLAogICAgInBhdGgiOiAiL255IiwKICAgICJwb3J0IjogNDQzMDAsCiAgICAicHMiOiAi8J+HrfCfh7BISy0xNi4xNjIuNTUuMTMwLTEyMzcxIiwKICAgICJ0bHMiOiAiIiwKICAgICJ0eXBlIjogImF1dG8iLAogICAgInNlY3VyaXR5IjogImF1dG8iLAogICAgInNraXAtY2VydC12ZXJpZnkiOiB0cnVlLAogICAgInNuaSI6ICIiCn0=
    ss://Y2hhY2hhMjAtaWV0Zi1wb2x5MTMwNTpHIXlCd1BXSDNWYW8=@162.251.61.221:812#%F0%9F%87%BA%F0%9F%87%B8US-162.251.61.221-0545
    ss://Y2hhY2hhMjAtaWV0Zi1wb2x5MTMwNTpHIXlCd1BXSDNWYW8=@196.247.59.156:811#%F0%9F%87%A8%F0%9F%87%A6CA-196.247.59.156-15770
    vmess://ewogICAgImFkZCI6ICIxMzkuOTkuOTEuOTUiLAogICAgImFpZCI6IDMyLAogICAgImhvc3QiOiAiIiwKICAgICJpZCI6ICJjMDE1NjQ1MS00ZWZiLTQ1ZTItODRmYy04ZDMxNWM0NjUwZGIiLAogICAgIm5ldCI6ICJ0Y3AiLAogICAgInBhdGgiOiAiIiwKICAgICJwb3J0IjogNDQzLAogICAgInBzIjogIvCfh7jwn4esU0ctMTM5Ljk5LjkxLjk1LTAyMzIiLAogICAgInRscyI6ICIiLAogICAgInR5cGUiOiAiYXV0byIsCiAgICAic2VjdXJpdHkiOiAiYXV0byIsCiAgICAic2tpcC1jZXJ0LXZlcmlmeSI6IHRydWUsCiAgICAic25pIjogIiIKfQ==
    ss://Y2hhY2hhMjAtaWV0Zi1wb2x5MTMwNTpHIXlCd1BXSDNWYW8=@37.120.147.230:810#%F0%9F%87%BA%F0%9F%87%B8US-37.120.147.230-10335
    ss://Y2hhY2hhMjAtaWV0Zi1wb2x5MTMwNTpHIXlCd1BXSDNWYW8=@38.91.107.225:812#%F0%9F%87%BA%F0%9F%87%B8US-38.91.107.225-15693
    ss://Y2hhY2hhMjAtaWV0Zi1wb2x5MTMwNTpHIXlCd1BXSDNWYW8=@196.247.59.156:808#%F0%9F%87%A8%F0%9F%87%A6CA-196.247.59.156-15691
    ss://YWVzLTI1Ni1jZmI6ZjYzZ2c4RXJ1RG5Vcm16NA==@213.183.59.214:9010#%F0%9F%87%B3%F0%9F%87%B1NL-213.183.59.214-17493
    vmess://ewogICAgImFkZCI6ICJzZy1vdmgxLnYyLXJheS5jb20iLAogICAgImFpZCI6IDAsCiAgICAiaG9zdCI6ICJzZy1vdmgxLnYyLXJheS5jb20iLAogICAgImlkIjogImE5NDgxNjAwLWVmMzYtNDAyYS1hMGU1LTU1NDdiZmQ3Yjg3YyIsCiAgICAibmV0IjogIndzIiwKICAgICJwYXRoIjogIi9mYXN0c3NoL2ZnaGhoLzYzNDE5N2M0Y2RmODEvIiwKICAgICJwb3J0IjogNDQzLAogICAgInBzIjogIvCfh7jwn4esU0ctNTEuNzkuMTY0LjE0Ni0yNzc4IiwKICAgICJ0bHMiOiAidGxzIiwKICAgICJ0eXBlIjogImF1dG8iLAogICAgInNlY3VyaXR5IjogImF1dG8iLAogICAgInNraXAtY2VydC12ZXJpZnkiOiB0cnVlLAogICAgInNuaSI6ICIiCn0=
    trojan://e05c749b-7c6b-41b8-9c71-9dcf685edf4a@152.67.162.166:443?allowInsecure=1&sni=content-provider22.cdn-delivery.akamaicd.com#%F0%9F%87%AE%F0%9F%87%B3IN-152.67.162.166-4645
    ss://Y2hhY2hhMjAtaWV0Zi1wb2x5MTMwNTpxWUF0ODVTRkdWNTY=@185.77.217.217:443#%F0%9F%87%AB%F0%9F%87%AEFI-185.77.217.217-0797
    ss://Y2hhY2hhMjAtaWV0Zi1wb2x5MTMwNTpHIXlCd1BXSDNWYW8=@38.114.114.139:811#%F0%9F%87%BA%F0%9F%87%B8US-38.114.114.139-10525
    ss://Y2hhY2hhMjAtaWV0Zi1wb2x5MTMwNTpHIXlCd1BXSDNWYW8=@196.247.59.156:804#%F0%9F%87%A8%F0%9F%87%A6CA-196.247.59.156-15768
    vmess://ewogICAgImFkZCI6ICJmdWxsYWNjZXNzdG9rb3JlYW5uZXRzdWJub2RlMS5henVyZXdlYnNpdGVzLm5ldCIsCiAgICAiYWlkIjogMCwKICAgICJob3N0IjogImZ1bGxhY2Nlc3N0b2tvcmVhbm5ldHN1Ym5vZGUxLmF6dXJld2Vic2l0ZXMubmV0IiwKICAgICJpZCI6ICIyNzRmMTFjNi1mNjliLTQwYjktODk2Ni1mMzllMDZlOTdiZTciLAogICAgIm5ldCI6ICJ3cyIsCiAgICAicGF0aCI6ICIvd3MiLAogICAgInBvcnQiOiA0NDMsCiAgICAicHMiOiAi8J+HsPCfh7dLUi01Mi4yMzEuMjAwLjE3OS01MDI5IiwKICAgICJ0bHMiOiAidGxzIiwKICAgICJ0eXBlIjogImF1dG8iLAogICAgInNlY3VyaXR5IjogImF1dG8iLAogICAgInNraXAtY2VydC12ZXJpZnkiOiB0cnVlLAogICAgInNuaSI6ICIiCn0=
    ss://Y2hhY2hhMjAtaWV0Zi1wb2x5MTMwNTpHIXlCd1BXSDNWYW8=@38.114.114.139:809#%F0%9F%87%BA%F0%9F%87%B8US-38.114.114.139-10984
    ss://Y2hhY2hhMjAtaWV0Zi1wb2x5MTMwNTpHIXlCd1BXSDNWYW8=@38.114.114.139:810#%F0%9F%87%BA%F0%9F%87%B8US-38.114.114.139-0772
    ss://Y2hhY2hhMjAtaWV0Zi1wb2x5MTMwNTpHIXlCd1BXSDNWYW8=@172.245.218.162:804#%F0%9F%87%BA%F0%9F%87%B8US-172.245.218.162-15753
    ss://Y2hhY2hhMjAtaWV0Zi1wb2x5MTMwNTpHIXlCd1BXSDNWYW8=@196.247.59.156:803#%F0%9F%87%A8%F0%9F%87%A6CA-196.247.59.156-15777
    ss://Y2hhY2hhMjAtaWV0Zi1wb2x5MTMwNTpHIXlCd1BXSDNWYW8=@162.251.61.47:800#%F0%9F%87%BA%F0%9F%87%B8US-162.251.61.47-15661
    ss://Y2hhY2hhMjAtaWV0Zi1wb2x5MTMwNTpHIXlCd1BXSDNWYW8=@172.245.218.162:800#%F0%9F%87%BA%F0%9F%87%B8US-172.245.218.162-21268
    ss://Y2hhY2hhMjAtaWV0Zi1wb2x5MTMwNTpHIXlCd1BXSDNWYW8=@172.245.218.162:805#%F0%9F%87%BA%F0%9F%87%B8US-172.245.218.162-15767
    vmess://ewogICAgImFkZCI6ICIxNjguMTM4LjIwNy42NiIsCiAgICAiYWlkIjogMCwKICAgICJob3N0IjogIiIsCiAgICAiaWQiOiAiOTA1Zjk5YjEtZTdiYS00NWUwLWFlNGQtYjBmZmRmMGFkMjQ1IiwKICAgICJuZXQiOiAidGNwIiwKICAgICJwYXRoIjogIiIsCiAgICAicG9ydCI6IDIxMzY1LAogICAgInBzIjogIvCfh6/wn4e1SlAtMTY4LjEzOC4yMDcuNjYtMDI2NyIsCiAgICAidGxzIjogIiIsCiAgICAidHlwZSI6ICJhdXRvIiwKICAgICJzZWN1cml0eSI6ICJhdXRvIiwKICAgICJza2lwLWNlcnQtdmVyaWZ5IjogdHJ1ZSwKICAgICJzbmkiOiAiIgp9
    ss://Y2hhY2hhMjAtaWV0Zi1wb2x5MTMwNTopMU4xRTZ2MFNVX3JHVHBn@79.133.109.56:1036#%F0%9F%87%BA%F0%9F%87%B8US-79.133.109.56-15762
    ss://Y2hhY2hhMjAtaWV0Zi1wb2x5MTMwNTpHIXlCd1BXSDNWYW8=@172.245.218.162:809#%F0%9F%87%BA%F0%9F%87%B8US-172.245.218.162-15775
    vmess://ewogICAgImFkZCI6ICJ3d3cuZ292LmhrIiwKICAgICJhaWQiOiAwLAogICAgImhvc3QiOiAidm4uY2xvdWRmbGFyZS5xdWVzdCIsCiAgICAiaWQiOiAiZGM4YjY0ZGItZWI2ZC00YmRmLTk4YjItMzE2MTUzMTliZWE4IiwKICAgICJuZXQiOiAid3MiLAogICAgInBhdGgiOiAiL2FyaWVzIiwKICAgICJwb3J0IjogMjA4NiwKICAgICJwcyI6ICLwn4+BUkVMQVktMTA0LjE2LjI0OS4xMzAtMTI5NSIsCiAgICAidGxzIjogIiIsCiAgICAidHlwZSI6ICJhdXRvIiwKICAgICJzZWN1cml0eSI6ICJhdXRvIiwKICAgICJza2lwLWNlcnQtdmVyaWZ5IjogdHJ1ZSwKICAgICJzbmkiOiAiIgp9
    vmess://ewogICAgImFkZCI6ICIxODUuMjI1LjY5LjEzNCIsCiAgICAiYWlkIjogMCwKICAgICJob3N0IjogIiIsCiAgICAiaWQiOiAiM2MzYmZkNzUtZGMzMC00ZTc2LTg5NDAtNDdlMTEzN2UyMWY5IiwKICAgICJuZXQiOiAidGNwIiwKICAgICJwYXRoIjogIiIsCiAgICAicG9ydCI6IDQ1MDgxLAogICAgInBzIjogIvCfh63wn4e6SFUtMTg1LjIyNS42OS4xMzQtMDIyMyIsCiAgICAidGxzIjogIiIsCiAgICAidHlwZSI6ICJhdXRvIiwKICAgICJzZWN1cml0eSI6ICJhdXRvIiwKICAgICJza2lwLWNlcnQtdmVyaWZ5IjogdHJ1ZSwKICAgICJzbmkiOiAiIgp9
    ss://Y2hhY2hhMjAtaWV0Zi1wb2x5MTMwNTpHIXlCd1BXSDNWYW8=@172.245.218.162:810#%F0%9F%87%BA%F0%9F%87%B8US-172.245.218.162-15761
    ss://Y2hhY2hhMjAtaWV0Zi1wb2x5MTMwNTpHIXlCd1BXSDNWYW8=@172.245.218.162:801#%F0%9F%87%BA%F0%9F%87%B8US-172.245.218.162-15719
    vmess://ewogICAgImFkZCI6ICJzZzExOC5oa2FhMC50ayIsCiAgICAiYWlkIjogMCwKICAgICJob3N0IjogInNnMTE4LmhrYWEwLnRrIiwKICAgICJpZCI6ICI2NTJmNDI2My1iZDg2LTRiZjYtOWY3ZS1kMjVlNzUxNmZiNzIiLAogICAgIm5ldCI6ICJ3cyIsCiAgICAicGF0aCI6ICIvaGthYTAiLAogICAgInBvcnQiOiAxMzY5MSwKICAgICJwcyI6ICLwn4e48J+HrFNHLTE3Mi4xMDQuMTYzLjExOC0wMjQ4IiwKICAgICJ0bHMiOiAiIiwKICAgICJ0eXBlIjogImF1dG8iLAogICAgInNlY3VyaXR5IjogImF1dG8iLAogICAgInNraXAtY2VydC12ZXJpZnkiOiB0cnVlLAogICAgInNuaSI6ICIiCn0=
    ss://Y2hhY2hhMjAtaWV0Zi1wb2x5MTMwNTpHIXlCd1BXSDNWYW8=@37.120.147.230:804#%F0%9F%87%BA%F0%9F%87%B8US-37.120.147.230-10332
    ss://Y2hhY2hhMjAtaWV0Zi1wb2x5MTMwNTpHIXlCd1BXSDNWYW8=@38.91.107.225:800#%F0%9F%87%BA%F0%9F%87%B8US-38.91.107.225-15681
    vmess://ewogICAgImFkZCI6ICJ2c2cxLjBiYWQuY29tIiwKICAgICJhaWQiOiAwLAogICAgImhvc3QiOiAiJTdCJTIySG9zdCUyMjolMjJ2c2cxLjBiYWQuY29tJTIyJTdEIiwKICAgICJpZCI6ICI5MjcwOTRkMy1kNjc4LTQ3NjMtODU5MS1lMjQwZDBiY2FlODciLAogICAgIm5ldCI6ICJ3cyIsCiAgICAicGF0aCI6ICIvY2hhdCIsCiAgICAicG9ydCI6IDQ0MywKICAgICJwcyI6ICLwn4e48J+HrFNHLTE3MC4xODcuMTk2LjEyOC0xNTk4MSIsCiAgICAidGxzIjogInRscyIsCiAgICAidHlwZSI6ICJhdXRvIiwKICAgICJzZWN1cml0eSI6ICJhdXRvIiwKICAgICJza2lwLWNlcnQtdmVyaWZ5IjogdHJ1ZSwKICAgICJzbmkiOiAiIgp9
    vmess://ewogICAgImFkZCI6ICI4OS4yMDguMTA1LjYzIiwKICAgICJhaWQiOiAwLAogICAgImhvc3QiOiAiIiwKICAgICJpZCI6ICIyRjA5NDg0NS1FMkJELUVCRjctREVCNy05OTU5OTI0MzZGQUYiLAogICAgIm5ldCI6ICJ0Y3AiLAogICAgInBhdGgiOiAiIiwKICAgICJwb3J0IjogMjM0NTMsCiAgICAicHMiOiAi8J+Hs/Cfh7FOTC04OS4yMDguMTA1LjYzLTAzMDYiLAogICAgInRscyI6ICJ0bHMiLAogICAgInR5cGUiOiAiYXV0byIsCiAgICAic2VjdXJpdHkiOiAiYXV0byIsCiAgICAic2tpcC1jZXJ0LXZlcmlmeSI6IHRydWUsCiAgICAic25pIjogIiIKfQ==
    ss://Y2hhY2hhMjAtaWV0Zi1wb2x5MTMwNTpHIXlCd1BXSDNWYW8=@38.91.107.225:802#%F0%9F%87%BA%F0%9F%87%B8US-38.91.107.225-15692
    ss://Y2hhY2hhMjAtaWV0Zi1wb2x5MTMwNTpHIXlCd1BXSDNWYW8=@195.12.49.82:812#%F0%9F%87%AC%F0%9F%87%A7GB-195.12.49.82-0765
    ss://Y2hhY2hhMjAtaWV0Zi1wb2x5MTMwNTpHIXlCd1BXSDNWYW8=@195.12.49.82:807#%F0%9F%87%AC%F0%9F%87%A7GB-195.12.49.82-20430
    ss://Y2hhY2hhMjAtaWV0Zi1wb2x5MTMwNTpHIXlCd1BXSDNWYW8=@37.120.219.218:812#%F0%9F%87%BA%F0%9F%87%B8US-37.120.219.218-15660
    trojan://3f087c04-44e6-4c96-a917-ca974de1212b@kr1.api-aws.com:443?allowInsecure=1#%F0%9F%87%B0%F0%9F%87%B7KR-146.56.176.239-15564
    ss://Y2hhY2hhMjAtaWV0Zi1wb2x5MTMwNTpHIXlCd1BXSDNWYW8=@37.120.147.230:803#%F0%9F%87%BA%F0%9F%87%B8US-37.120.147.230-10337
    vmess://ewogICAgImFkZCI6ICIxNzIuNjQuMTUzLjEwMiIsCiAgICAiYWlkIjogMCwKICAgICJob3N0IjogImNsYXNoMi50cnVtcDIwMjMudXMiLAogICAgImlkIjogImJlZDNkODc2LTJkMjYtNGQ0ZC1iNzg5LTMwNjM0MzhlZTc3NCIsCiAgICAibmV0IjogIndzIiwKICAgICJwYXRoIjogIi9kb25ndGFpd2FuZy5jb20iLAogICAgInBvcnQiOiA0NDMsCiAgICAicHMiOiAi8J+PgVJFTEFZLTE3Mi42NC4xNTMuMTAyLTAyNTIiLAogICAgInRscyI6ICJ0bHMiLAogICAgInR5cGUiOiAiYXV0byIsCiAgICAic2VjdXJpdHkiOiAiYXV0byIsCiAgICAic2tpcC1jZXJ0LXZlcmlmeSI6IHRydWUsCiAgICAic25pIjogIiIKfQ==
    ss://Y2hhY2hhMjAtaWV0Zi1wb2x5MTMwNTpHIXlCd1BXSDNWYW8=@195.12.49.82:805#%F0%9F%87%AC%F0%9F%87%A7GB-195.12.49.82-20428
    ss://Y2hhY2hhMjAtaWV0Zi1wb2x5MTMwNTpHIXlCd1BXSDNWYW8=@195.12.49.82:801#%F0%9F%87%AC%F0%9F%87%A7GB-195.12.49.82-2879
    ss://Y2hhY2hhMjAtaWV0Zi1wb2x5MTMwNTpHIXlCd1BXSDNWYW8=@195.12.49.82:810#%F0%9F%87%AC%F0%9F%87%A7GB-195.12.49.82-20415
    ss://Y2hhY2hhMjAtaWV0Zi1wb2x5MTMwNTpHIXlCd1BXSDNWYW8=@195.12.49.82:808#%F0%9F%87%AC%F0%9F%87%A7GB-195.12.49.82-20437
    ss://Y2hhY2hhMjAtaWV0Zi1wb2x5MTMwNTpHIXlCd1BXSDNWYW8=@195.12.49.82:802#%F0%9F%87%AC%F0%9F%87%A7GB-195.12.49.82-20423
    vmess://ewogICAgImFkZCI6ICJ1bnVzMDEuYWpka2phbGpkai54eXoiLAogICAgImFpZCI6IDAsCiAgICAiaG9zdCI6ICJ1bnVzMDEuYWpka2phbGpkai54eXoiLAogICAgImlkIjogIjk1ZTlmZGExLWRjNDgtM2JiZC04YTE1LWU2NTI4ODgyZWEzYiIsCiAgICAibmV0IjogIndzIiwKICAgICJwYXRoIjogIi82IiwKICAgICJwb3J0IjogMTA4MiwKICAgICJwcyI6ICLwn4e68J+HuFVTLTM4LjU0Ljk1LjE3OC01MjQxIiwKICAgICJ0bHMiOiAiIiwKICAgICJ0eXBlIjogImF1dG8iLAogICAgInNlY3VyaXR5IjogImF1dG8iLAogICAgInNraXAtY2VydC12ZXJpZnkiOiB0cnVlLAogICAgInNuaSI6ICIiCn0=
    ss://Y2hhY2hhMjAtaWV0Zi1wb2x5MTMwNTpHIXlCd1BXSDNWYW8=@195.12.49.82:800#%F0%9F%87%AC%F0%9F%87%A7GB-195.12.49.82-20418
    ss://Y2hhY2hhMjAtaWV0Zi1wb2x5MTMwNTpHIXlCd1BXSDNWYW8=@185.104.184.78:800#%F0%9F%87%A9%F0%9F%87%B0DK-185.104.184.78-4617
    ss://Y2hhY2hhMjAtaWV0Zi1wb2x5MTMwNTpHIXlCd1BXSDNWYW8=@51.159.30.61:808#%F0%9F%87%AB%F0%9F%87%B7FR-51.159.30.61-0082
    ss://Y2hhY2hhMjAtaWV0Zi1wb2x5MTMwNTpHIXlCd1BXSDNWYW8=@193.176.86.190:806#%F0%9F%87%A9%F0%9F%87%AADE-193.176.86.190-0969
    ss://Y2hhY2hhMjAtaWV0Zi1wb2x5MTMwNTpHIXlCd1BXSDNWYW8=@185.104.184.78:801#%F0%9F%87%A9%F0%9F%87%B0DK-185.104.184.78-0967
    ss://Y2hhY2hhMjAtaWV0Zi1wb2x5MTMwNTpHIXlCd1BXSDNWYW8=@185.104.184.78:806#%F0%9F%87%A9%F0%9F%87%B0DK-185.104.184.78-0763
    ss://Y2hhY2hhMjAtaWV0Zi1wb2x5MTMwNTpHIXlCd1BXSDNWYW8=@37.120.219.218:801#%F0%9F%87%BA%F0%9F%87%B8US-37.120.219.218-15655
    vmess://ewogICAgImFkZCI6ICIyMTMuMjI2LjcxLjEyNyIsCiAgICAiYWlkIjogMCwKICAgICJob3N0IjogIiIsCiAgICAiaWQiOiAiMkYwOTQ4NDUtRTJCRC1FQkY3LURFQjctOTk1OTkyNDM2RkFGIiwKICAgICJuZXQiOiAidGNwIiwKICAgICJwYXRoIjogIiIsCiAgICAicG9ydCI6IDIzNDUzLAogICAgInBzIjogIvCfh6nwn4eqREUtMjEzLjIyNi43MS4xMjctNzkyNCIsCiAgICAidGxzIjogInRscyIsCiAgICAidHlwZSI6ICJhdXRvIiwKICAgICJzZWN1cml0eSI6ICJhdXRvIiwKICAgICJza2lwLWNlcnQtdmVyaWZ5IjogdHJ1ZSwKICAgICJzbmkiOiAiIgp9
    ss://Y2hhY2hhMjAtaWV0Zi1wb2x5MTMwNTpHIXlCd1BXSDNWYW8=@185.104.184.78:807#%F0%9F%87%A9%F0%9F%87%B0DK-185.104.184.78-7529
    vmess://ewogICAgImFkZCI6ICJzZy5wcnByLmxpbmsiLAogICAgImFpZCI6IDAsCiAgICAiaG9zdCI6ICJzZy5wcnByLmxpbmsiLAogICAgImlkIjogImNlYTQyMTYxLWJkZGMtNDIzMC1hOWI5LWU0MzE4Nzk2N2ZmYSIsCiAgICAibmV0IjogIndzIiwKICAgICJwYXRoIjogIi9UZWxlZ3JhbS9TaGFyZUNlbnRyZVByby9ta25uaXgiLAogICAgInBvcnQiOiA0NDMsCiAgICAicHMiOiAi8J+PgVJFTEFZLTEwNC4yMS4zNS4yMTEtMTI1OCIsCiAgICAidGxzIjogInRscyIsCiAgICAidHlwZSI6ICJhdXRvIiwKICAgICJzZWN1cml0eSI6ICJhdXRvIiwKICAgICJza2lwLWNlcnQtdmVyaWZ5IjogdHJ1ZSwKICAgICJzbmkiOiAiIgp9
    ss://Y2hhY2hhMjAtaWV0Zi1wb2x5MTMwNTpHIXlCd1BXSDNWYW8=@185.104.184.78:809#%F0%9F%87%A9%F0%9F%87%B0DK-185.104.184.78-7524
    ss://Y2hhY2hhMjAtaWV0Zi1wb2x5MTMwNTpHIXlCd1BXSDNWYW8=@185.104.184.78:810#%F0%9F%87%A9%F0%9F%87%B0DK-185.104.184.78-2099
    ss://Y2hhY2hhMjAtaWV0Zi1wb2x5MTMwNTpHIXlCd1BXSDNWYW8=@185.104.184.78:804#%F0%9F%87%A9%F0%9F%87%B0DK-185.104.184.78-7527
    ss://Y2hhY2hhMjAtaWV0Zi1wb2x5MTMwNTpHIXlCd1BXSDNWYW8=@185.104.184.78:808#%F0%9F%87%A9%F0%9F%87%B0DK-185.104.184.78-7521
    ss://Y2hhY2hhMjAtaWV0Zi1wb2x5MTMwNTpHIXlCd1BXSDNWYW8=@51.159.30.61:809#%F0%9F%87%AB%F0%9F%87%B7FR-51.159.30.61-1423
    ss://Y2hhY2hhMjAtaWV0Zi1wb2x5MTMwNTpHIXlCd1BXSDNWYW8=@185.104.184.78:802#%F0%9F%87%A9%F0%9F%87%B0DK-185.104.184.78-7526
    ss://Y2hhY2hhMjAtaWV0Zi1wb2x5MTMwNTpVbHRyQHIwMHRfMjAxNw==@138.68.248.130:811#%F0%9F%87%BA%F0%9F%87%B8US-138.68.248.130-0556

</details>

- you can import these 200 tested nodes using their subscription link into different clients. refer to `Instructions & Usage` section

### all nodes
merge nodes w/o dup: `352`
- [Node link Mixed (V2ray)](https://raw.githubusercontent.com/mahdibland/ShadowsocksAggregator/master/sub/sub_merge.txt)
- [Node link Yaml (Clash)](https://raw.githubusercontent.com/mahdibland/SSAggregator/master/sub/sub_merge_yaml.yml)

#### all nodes separated by protoctol
- [VMESS](https://raw.githubusercontent.com/mahdibland/ShadowsocksAggregator/master/sub/splitted/vmess.txt)
- [TROJAN](https://raw.githubusercontent.com/mahdibland/ShadowsocksAggregator/master/sub/splitted/trojan.txt)
- [SSR](https://raw.githubusercontent.com/mahdibland/ShadowsocksAggregator/master/sub/splitted/ssr.txt)
- [SHADOWSOCKS](https://raw.githubusercontent.com/mahdibland/ShadowsocksAggregator/master/sub/splitted/ss.txt)

#### provider config for clash 🐈‍⬛
> Configs with the "others" tag will proxy domestic services.

- [Clash Meta For Iran](https://cdn.jsdelivr.net/gh/mahdibland/V2RayAggregator@master/update/provider/provider-meta.yml) (Recommended)
- [Clash Meta For China](https://cdn.jsdelivr.net/gh/mahdibland/V2RayAggregator@master/update/provider/provider-meta-cn.yml) (Recommended)
- [Clash Meta For Others](https://cdn.jsdelivr.net/gh/mahdibland/V2RayAggregator@master/update/provider/provider-meta-others.yml) (Recommended)

- [Clash For Iran](https://cdn.jsdelivr.net/gh/mahdibland/V2RayAggregator@master/update/provider/provider.yml)
- [Clash For China](https://cdn.jsdelivr.net/gh/mahdibland/V2RayAggregator@master/update/provider/provider-cn.yml)
- [Clash For Others](https://cdn.jsdelivr.net/gh/mahdibland/V2RayAggregator@master/update/provider/provider-others.yml)


### node sources
- [ermaozi/get_subscribe](https://github.com/ermaozi/get_subscribe), number of nodes: `18`
- [anaer/Sub](https://github.com/anaer/Sub), number of nodes: `36`
- [aiboboxx/v2rayfree](https://github.com/aiboboxx/v2rayfree), number of nodes: `128`
- [Pawdroid/Free-servers](https://github.com/Pawdroid/Free-servers), number of nodes: `22`
- [mfuu/v2ray](https://github.com/mfuu/v2ray), number of nodes: `534`
- [peasoft/NoMoreWalls](https://github.com/peasoft/NoMoreWalls), number of nodes: `140`

## Softwares

### Best Clients For Each OS

|    OS   |              Best Client               | Alternatives |
|:-------:|:--------------------------------------:|:------------:|
|   IOS   |        Quantumult - Shadowrocket       |  NapsternetV |
| Android |Surfboard - Clash For Android - Matsuri |    V2rayNg   |
| Windows |   Clash For Windows - V2rayN - Nekoray |    Qv2ray    |
|  Linux  |           Clash For Windows            |    Qv2ray    |
|  MacOS  |           Clash For Windows            |    Qv2ray    |

### Desktop Clients

|                              MacOS                               |                              Linux                               |                                       Windows                                       | Brief description                                                                                         |
| :--------------------------------------------------------------: | :--------------------------------------------------------------: | :---------------------------------------------------------------------------------: | :----------------------------------------------------------------------------------------------- |
| [CFW](https://github.com/Fndroid/clash_for_windows_pkg/releases) | [CFW](https://github.com/Fndroid/clash_for_windows_pkg/releases) | [CFW(Clash For Windows)](https://github.com/Fndroid/clash_for_windows_pkg/releases) | SS, SSR, Trojan, Vmess, VLESS protocol support, strong policy offload capability.                                         |
|       [Qv2ray](https://github.com/Qv2ray/Qv2ray/releases)        |       [Qv2ray](https://github.com/Qv2ray/Qv2ray/releases)        |                 [Qv2ray](https://github.com/Qv2ray/Qv2ray/releases)                 | SS, SSR, Trojan, Vmess, VLESS, Trojan-Go protocol support (relevant plugins need to be installed).                            |
|                                ×                                 |                                ×                                 |                 [V2rayN](https://github.com/2dust/v2rayN/releases)                  | SS, Trojan, Vmess, VLESS protocol support, with speed measurement, delay measurement function, support subscription, QR code, clipboard import and manual configuration.  |
|                                ×                                 |                                ×                                 |               [WinXray](https://github.com/TheMRLL/winxray/releases)                | SS, SSR, Trojan, Vmess, VLESS protocol support, support automatic connection to the fastest node.                                   |
|                                ×                                 |                                ×                                 | [Shadowsocks-windows](https://github.com/shadowsocks/shadowsocks-windows/releases)  | SS protocol support, SS dedicated client.                                                                    |
|                                ×                                 |                                ×                                 |  [ShadowsocksR-windows](https://github.com/HMBSbige/ShadowsocksR-Windows/releases)  | SSR protocol support, SSR dedicated client.                                                                   |
|                  [Surge](https://nssurge.com/)                   |                                ×                                 |                                          ×                                          | SS, Trojan, Vmess protocol support, well-known network debugging tools, powerful strategy offloading ability, need to pay.                         |
|     [ClashX](https://github.com/yichengchen/clashX/releases)     |                                ×                                 |                                          ×                                          | SS, SSR, Trojan, Vmess protocol support, occupy less resources.                                                  |
|        [V2rayU](https://github.com/yanue/V2rayU/releases)        |                                ×                                 |                                          ×                                          | SS, Trojan, Vmess protocol support, support subscription, QR code, clipboard import, manual configuration, QR code sharing, similar to V2RayN. |
|       [V2rayA](https://github.com/v2rayA/v2rayA/releases/)       |       [V2rayA](https://github.com/v2rayA/v2rayA/releases/)       |                [V2rayA](https://github.com/v2rayA/v2rayA/releases/)                 | V2Ray, Xray, SS, SSR, Trojan support, subscription and manual config.  |

### Mobile Clients

|                               iOS/iPadOS                                |                                      Android                                       | Brief description                                                                                                                                                  |
| :---------------------------------------------------------------------: | :--------------------------------------------------------------------------------: | --------------------------------------------------------------------------------------------------------------------------------------------------------- |
| [Shadowrocket](https://apps.apple.com/us/app/shadowrocket/id932747118)  |  [Shadowrocket](https://play.google.com/store/apps/details?id=com.v2cross.proxy)   | SS, SSR, Trojan, Vmess, VLESS protocol support, the iOS side needs to be purchased in the non-country App Store, the US price is $2.99; the Android side is not the same author as the iOS side, does not support the SSR protocol, free and built-in free nodes. |
|                      [Surge](https://nssurge.com/)                      |                                         ×                                          | SS, Trojan, Vmess protocol support, well-known network debugging tools on the iOS side, chargeable.                                                                                              |
| [Quantumult X](https://apps.apple.com/us/app/quantumult-x/id1443988620) |                                         ×                                          |                                                                                 |
| [Potatso Lite](https://apps.apple.com/us/app/potatso-lite/id1239860606) |                                         ×                                          | SS, SSR protocol support, need to be purchased in the non-country AppStore, free.                                                                                                        |
|                                    ×                                    |    [Surfboard](https://play.google.com/store/apps/details?id=com.getsurfboard)     | SS, SSR, Vmess Protocol support, Android network debugging software, compatible with Surge 2 configuration.                                                                                          |
|                                    ×                                    |    [CFA(Clash For Android)](https://github.com/Kr328/ClashForAndroid/releases)     | SS, SSR, Trojan, Vmess Protocol support.                                                                                                                         |
|                                    ×                                    |             [SagerNet](https://github.com/SagerNet/SagerNet/releases)              | SS, SSR, Trojan, Vmess, VLESS Protocol support.                                                                                                                  |
|                                    ×                                    | [Shadowsocks-android](https://github.com/shadowsocks/shadowsocks-android/releases) | SS protocol support, Android-specific SS client.                                                                                                                         |
|                                    ×                                    | [ShadowsocksR-android](https://github.com/HMBSbige/ShadowsocksR-Android/releases)  | SSR protocol support, Android-specific SSR client.                                                                                                                       |
|                                    ×                                    |                [V2rayNG](https://github.com/2dust/v2rayNG/releases)                | SS, Trojan, Vmess, VLESS protocol support, v2ray kernel.                                                                                                           |

### Credit: 
- [alanbobs999](https://github.com/alanbobs999)
- [PersianBlocker](https://github.com/MasterKia/PersianBlocker)
- [iran-hosted-domains](https://github.com/bootmortis/iran-hosted-domains)
