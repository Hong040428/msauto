# 用cloudflare的workers实现自助创建微软全局子号
# demo: https://m.ur.workers.dev/


1 进入 `Azure Active Directory` 新建一个 `app`，获取 `tenant id` 和 `client id`
![image.png](https://i.loli.net/2020/01/26/57GcEDYlQFTOMBL.png)

2.给 `app` 授权，权限为 `graph` 的 `Directory.ReadWrite.All`
![image.png](https://i.loli.net/2020/05/06/NOE18pDfj4QwRAP.png)

3 新建一个 `client secret`
![image.png](https://i.loli.net/2020/01/26/qUeV2x8abHlDPO3.png)

4 获取 skuid 
> 在 Microsoft 365 admin center 管理面板-账单-许可证
> 然后点击你想看的「许可证」，在地址栏就有 skuid 了



5 复制 `worker.js` 里面的内容到 `cf workers` 里面，填入相应的数据
