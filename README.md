## Tunnel 4-0-4

## Workers Deployment Methods
1. Deploy CF Worker:
- Create a new Worker in the CF Worker console.
- Paste the contents of [worker.js](https://github.com/nyeinkokoaung404/tunnel404/blob/main/_worker.js) into the Worker editor.
- Change line 7 `userID` to your own **UUID**.

2. Access subscription content:
- Visit `https://[YOUR-WORKERS-URL]/[UUID]` to get the subscription content.
- For example, `https://vless.google.workers.dev/90cd4a77-141a-43c9-991b-08263cfe9c10` is your universal adaptive subscription address.
- For example, `https://vless.google.workers.dev/90cd4a77-141a-43c9-991b-08263cfe9c10?sub` Base64 subscription format, suitable for PassWall, SSR+, etc.
- For example, `https://vless.google.workers.dev/90cd4a77-141a-43c9-991b-08263cfe9c10?clash` Clash subscription format, suitable for OpenClash, etc.
- For example, `https://vless.google.workers.dev/90cd4a77-141a-43c9-991b-08263cfe9c10?sb` singbox subscription format, suitable for singbox, etc.

3. Bind custom domains to workers: 
- In the workers console, on the `Triggers` tab, click `Add custom domain`.
- Fill in the subdomain you have transferred to the CF domain name resolution service, for example: `vless.google.com`, then click `Add custom domain` and wait for the certificate to take effect.
- **If you are a newbie, you can take off now, no need to read on! ! ! **

<details>
<summary><code><strong>" I am not a newbie! I really am not a newbie! I want to play tricks! I want to start high-end gameplay!"</strong></code></summary>

4. Subscriptions using your own `preferred domain name`/`preferred IP`：
   - If you want to use your own preferred domain name or preferred IP, you can refer to the deployment instructions in the [WorkerVless2sub GitHub repository](https://github.com/nyeinkokoaung404/WorkerVless2sub) to build it yourself.
- Open the [worker.js](https://github.com/nyeinkokoaung404/tunnel404/blob/main/_worker.js) file, find the `sub` variable in line 12, and modify it to the subscription generator address you deployed. For example, `let sub = 'sub.cmliussss.workers.dev';`, be careful not to include protocol information and symbols such as https.
- Note that if you use your own subscription address, the subscription generator's `sub` domain name and the domain name of `[YOUR-WORKER-URL]` must not belong to the same top-level domain name, otherwise an exception will occur. You can assign the domain name assigned to workers.dev to the `sub` variable.

</details>

## Pages Upload Deployment Method **Best Recommended!!!**
1. Deploy CF Pages:
- Download the [main.zip](https://github.com/nyeinkokoaung404/tunnel404/archive/refs/heads/main.zip) file and click Star!!!
- In the CF Pages console, select `Upload assets`, name your project and click `Create project`, then upload the downloaded [main.zip](https://github.com/nyeinkokoaung404/tunnel404/archive/refs/heads/main.zip) file and click `Deploy site`.
- After the deployment is complete, click `Continue working on site`, select `Settings` > `Environment variables` > **Make** define variables for production environment > `Add variable`.
Fill in **UUID** for the variable name and your UUID for the value, then click `Save`.
- Return to the `Deployment` tab, click `Create New Deployment` in the lower right corner, re-upload the [main.zip](https://github.com/nyeinkokoaung404/tunnel404/archive/refs/heads/main.zip) file, and click `Save and Deploy`.

2. Access Subscription Content:
- Visit `https://[YOUR-PAGES-URL]/[YOUR-UUID]` to get the subscription content.
- For example, `https://edgetunnel.pages.dev/90cd4a77-141a-43c9-991b-08263cfe9c10` is your universal adaptive subscription address.
- For example, `https://edgetunnel.pages.dev/90cd4a77-141a-43c9-991b-08263cfe9c10?sub` Base64 subscription format, suitable for PassWall, SSR+, etc.
- For example, `https://edgetunnel.pages.dev/90cd4a77-141a-43c9-991b-08263cfe9c10?clash` Clash subscription format, suitable for OpenClash, etc.
- For example, `https://edgetunnel.pages.dev/90cd4a77-141a-43c9-991b-08263cfe9c10?sb` singbox subscription format, suitable for singbox, etc.

<details>
<summary><code><strong>「 I have my own domain name! I want to bind my own domain name! I have mastered domain name resolution! 」</strong></code></summary>

3. Bind a CNAME custom domain to Pages
- In the `Custom Domain` tab of the Pages console, click `Set Custom Domain` at the bottom.
- Fill in your custom subdomain name, and be careful not to use your root domain name, for example:
If the domain name you are assigned is `fuck.cloudns.biz`, then add a custom domain and fill in `lizi.fuck.cloudns.biz`;
- According to the requirements of CF, your domain name DNS service provider will be returned. After adding the CNAME record `edgetunnel.pages.dev` of the custom domain `lizi`, click `Activate Domain`.
- **If you are a novice, then your pages can take off directly after binding the `custom domain`, no need to read on! ! ! **
-
</details>
<details>
<summary><code><strong>「 I am not a newbie! I am really not a newbie! I want to play tricks! I want to open up high-end gameplay! 」</strong></code></summary>

4. Subscription content using your own `preferred domain name`/`preferred IP`:
- If you want to use your own preferred domain name or your own preferred IP, you can refer to the deployment instructions in the [WorkerVless2sub GitHub repository](https://github.com/nyeinkokoaung404/WorkerVless2sub) to build it yourself.
- In the `Settings` tab of the Pages console, select `Environment variables` > `Make` > `Edit variables` > `Add variable`;
- Set the variable name to `SUB`, and the corresponding value is the subscription generator address you deployed. For example, `sub.cmliussss.workers.dev`, and then click **Save**.
- Then, in the `Deployment` tab of the Pages console, select `All Deployments` > `Latest Deployment` > `Retry Deployment`.
- Note that if you use your own subscription address, the `SUB` domain name of the subscription generator and the domain name of `[YOUR-PAGES-URL]` must not belong to the same top-level domain name, otherwise an exception will occur. You can assign the domain name assigned to Pages.dev to the `SUB` variable.

</details>

## Pages GitHub Deployment Methods
1. Deploy CF Pages:
- Fork this project on Github and click Star!!!
- In the CF Pages console, select `Connect to Git`, select the `edgetunnel` project and click `Start Setup`.
- Under the `Set Build and Deployment` page, select `Environment Variables (Advanced)` and `Add Variable`
Fill in **UUID** as the variable name and your UUID as the value, then click `Save and Deploy`.

2. Access Subscription Content:
- Visit `https://[YOUR-PAGES-URL]/[YOUR-UUID]` to get the subscription content.
- For example, `https://edgetunnel.pages.dev/90cd4a77-141a-43c9-991b-08263cfe9c10` is your universal adaptive subscription address.
- For example, `https://edgetunnel.pages.dev/90cd4a77-141a-43c9-991b-08263cfe9c10?sub` Base64 subscription format, suitable for PassWall, SSR+, etc.
- For example, `https://edgetunnel.pages.dev/90cd4a77-141a-43c9-991b-08263cfe9c10?clash` Clash subscription format, suitable for OpenClash, etc.
- For example, `https://edgetunnel.pages.dev/90cd4a77-141a-43c9-991b-08263cfe9c10?sb` singbox subscription format, suitable for singbox, etc.

3. Bind a CNAME custom domain to Pages
- In the `Custom Domains` tab of the Pages console, click `Set Custom Domain` at the bottom.
- Fill in your custom subdomain name, be careful not to use your root domain name, for example:
If the domain name you are assigned is `fuck.cloudns.biz`, then add a custom domain and fill in `lizi.fuck.cloudns.biz`;
- According to CF's requirements, your domain name DNS service provider will be returned. After adding the CNAME record `edgetunnel.pages.dev` of the custom domain `lizi`, click `Activate Domain`.
- **If you are a newbie, then your pages can take off directly after binding the `custom domain`, no need to read on! ! ! **

<details>
<summary><code><strong>" I am not a newbie! I am really not a newbie! I want to play tricks! I want to open up high-end gameplay!"</strong></code></summary>

4. Subscriptions using your own `preferred domain name`/`preferred IP`:
- If you want to use your own preferred domain name or your own preferred IP, you can refer to the deployment instructions in the [WorkerVless2sub GitHub repository](https://github.com/nyeinkokoaung404/WorkerVless2sub) to build it yourself.
- In the `Settings` tab of the Pages console, select `Environment variables` > `Make` > `Edit variables` > `Add variable`;
- Set the variable name to `SUB`, and the corresponding value is the address of the subscription generator you deployed. For example, `sub.cmliussss.workers.dev`, and then click **Save**.
- Then in the `Deployments` tab of the Pages console, select `All deployments` > `Latest deployment rightmost ...` > `Retry deployment`, and that's it.
- Note that if you use your own subscription address, the `SUB` domain name of the subscription generator and the domain name of `[YOUR-PAGES-URL]` must not belong to the same top-level domain, otherwise an exception will occur. You can assign the domain assigned to Pages.dev to the `SUB` variable.

</details>

## Variable Description
| Variable Name | Example | Required | Notes | YT |
|--------|---------|-|-----|-----|
| UUID | `90cd4a77-141a-43c9-991b-08263cfe9c10` |✅| Powershell -NoExit -Command "[guid]::NewGuid()"| [Video](https://www.youtube.com/watch?v=s91zjpw3-P8&t=72s) |
| PROXYIP | `proxyip.fxxk.dedyn.io` |❌| Alternative proxy node for accessing CFCDN sites (supports multiple ProxyIPs, with `,` or `newline` as separators between ProxyIPs) | [Video](https://www.youtube.com/watch?v=s91zjpw3-P8&t=166s) |
| SOCKS5  | `user:password@127.0.0.1:1080` |❌| 优先作为访问CFCDN站点的SOCKS5代理(支持多socks5, socks5之间使用`,`或`换行`作间隔) | [Video](https://www.youtube.com/watch?v=s91zjpw3-P8&t=826s) |
| GO2SOCKS5  | `blog.cmliussss.com`,`*ip111.cn` |❌| 设置`SOCKS5`变量之后，可设置强制使用socks5访问名单(`*`可作为通配符，`换行`作多元素间隔) ||
| ADD | `icook.tw:2053#官方优选域名` |❌| 本地优选TLS域名/优选IP(支持多元素之间`,`或`换行`作间隔) ||
| ADDAPI | [https://raw.github.../addressesapi.txt](https://raw.githubusercontent.com/cmliu/WorkerVless2sub/main/addressesapi.txt) |❌| 优选IP的API地址(支持多元素之间`,`或 换行 作间隔) ||
| ADDNOTLS | `icook.hk:8080#官方优选域名` |❌| 本地优选noTLS域名/优选IP(支持多元素之间`,`或`换行`作间隔) ||
| ADDNOTLSAPI | [https://raw.github.../addressesapi.txt](https://raw.githubusercontent.com/cmliu/CFcdnVmess2sub/main/addressesapi.txt) |❌| 优选IP的API地址(支持多元素之间`,`或 换行 作间隔) ||
| ADDCSV | [https://raw.github.../addressescsv.csv](https://raw.githubusercontent.com/cmliu/WorkerVless2sub/main/addressescsv.csv) |❌| iptest测速结果(支持多元素, 元素之间使用`,`作间隔) ||
| DLS | `8` |❌| `ADDCSV`测速结果满足速度下限 ||
| TGTOKEN | `6894123456:XXXXXXXXXX0qExVsBPUhHDAbXXX` |❌| 发送TG通知的机器人token | 
| TGID | `6946912345` |❌| 接收TG通知的账户数字ID | 
| SUB | `VLESS.fxxk.dedyn.io` | ❌ | 内建域名、IP节点信息的订阅生成器地址 | [Video](https://www.youtube.com/watch?v=s91zjpw3-P8&t=1193s) |
| SUBAPI | `SUBAPI.fxxk.dedyn.io` |❌| clash、singbox等 订阅转换后端 | [Video](https://www.youtube.com/watch?v=s91zjpw3-P8&t=1446s) |
| SUBCONFIG | [https://raw.github.../ACL4SSR_Online_Full_MultiMode.ini](https://raw.githubusercontent.com/cmliu/ACL4SSR/main/Clash/config/ACL4SSR_Online_Full_MultiMode.ini) |❌| clash、singbox等 订阅转换配置文件 | [Video](https://www.youtube.com/watch?v=s91zjpw3-P8&t=1605s) |
| SUBNAME | `edgetunnel` |❌| 订阅名称 | |
| RPROXYIP | `false` |❌| 设为 true 即可强制获取订阅器分配的ProxyIP(需订阅器支持)| [Video](https://www.youtube.com/watch?v=s91zjpw3-P8&t=1816s) |
| URL302 | `https://t.me/CMLiussss` |❌| 主页302跳转(支持多url, url之间使用`,`或`换行`作间隔, 小白别用) |  |
| URL | `https://t.me/CMLiussss` |❌| 主页伪装(支持多url, url之间使用`,`或`换行`作间隔, 乱设容易触发反诈) |  |
| CFEMAIL | `admin@gmail.com` |❌| CF账户邮箱(与`CFKEY`都填上后, 订阅信息将显示请求使用量, 小白别用) |  |
| CFKEY | `c6a944b5c956b6c18c2352880952bced8b85e` |❌| CF账户Global API Key(与`CFEMAIL`都填上后, 订阅信息将显示请求使用量, 小白别用) |  |

**Note: After filling in `SOCKS5`, `PROXYIP` will no longer be enabled! Please choose one of the two! ! ! **

**Note: After filling in `SUB`, the subscription content generated by the `ADD*` class variables will no longer be enabled! Please choose one of the two! ! ! **

**Note: Filling in `CFEMAIL` and `CFKEY` at the same time will enable the display of request usage, but it is not recommended! There is no need to give a Worker project such high permissions! You are at your own risk! ! ! **

## Star ကြယ်တွေတက်လာတယ်။
[![Stargazers over time](https://starchart.cc/nyeinkokoaung404/tunnel404.svg?variant=adaptive)](https://starchart.cc/nyeinkokoaung404/tunnel404)

## Adaptive subscription content
   - [v2rayN](https://github.com/2dust/v2rayN)
   - clash.meta（[clash-verge-rev
](https://github.com/clash-verge-rev/clash-verge-rev)，[Clash Nyanpasu](https://github.com/keiko233/clash-nyanpasu)，~[clash-verge](https://github.com/zzzgydi/clash-verge/tree/main)~，ClashX Meta）
   - sing-box（SFI）
