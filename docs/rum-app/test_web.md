# Rum 网页版内测

使用浏览器 打开 http://wasmapp.rumsystem.net/ ，推荐采用 谷歌 Chrome 浏览器/Safari  

## 推荐加入已有种子网络

```seed
{
  "genesis_block": {
    "BlockId": "7ea204cd-cf74-4bc7-b34f-abd2d2405047",
    "GroupId": "18fe26fe-1cd8-415e-9f58-b0fca6b7fcf1",
    "ProducerPubKey": "CAISIQLqFnYwh2eCrQehiCzasJ0ZP8ZSqjFhO4ZdEN8fUPDGmw==",
    "Hash": "dxo1H5nMz/ipQhHnwr61zIV6KZa4bhCH6qNul5CKVRU=",
    "Signature": "MEUCIB48HKxrLtTSW/UlZL/x8aYgiUr6Ol37OXlxC8Xk0xXwAiEAi2lAbM2z2LVsTOkRMXcm3dPfgWi4uVmtIlKLMC0p7aU=",
    "TimeStamp": "1634699446630756189"
  },
  "group_id": "18fe26fe-1cd8-415e-9f58-b0fca6b7fcf1",
  "group_name": "来小酌一杯吧",
  "owner_pubkey": "CAISIQLqFnYwh2eCrQehiCzasJ0ZP8ZSqjFhO4ZdEN8fUPDGmw==",
  "consensus_type": "poa",
  "encryption_type": "public",
  "cipher_key": "c3206a5ff89c3152c3ed92fcabc18ef52d05a587bc77e88cd088c9167ed90de4",
  "app_key": "group_timeline",
  "signature": "304402207ee3dcf486cd556a0c6e139551819379efd5675bc47d6d1b037782aa9843f53b02203149a755e389f1865fc7d6aa6b1aebcdbc57ca203f206a4fe255c77b87e93616"
}

```

```seed
{
  "genesis_block": {
    "BlockId": "3d36c86c-af09-45e8-8823-8cb2471af0c0",
    "GroupId": "f1bcdebd-4f1d-43b9-89d0-88d5fc896660",
    "ProducerPubKey": "CAISIQLdBmr7WXMFgZhsBgx5+sAAGYKGzc8Agq9kGWhDZVqRpg==",
    "Hash": "DMONei13+u79APa0k7Nla91CDpeAQaKmvJsTqd5VIt8=",
    "Signature": "MEQCIB5bVuWmUQpzfWuaaUNPwKVsQSc4WdZCl3+kseHfU8VfAiA0KOjj0myzYBsjHmiZp5tAn4xEacEstPsG79wO2QLBBg==",
    "TimeStamp": "1640673495282521500"
  },
  "group_id": "f1bcdebd-4f1d-43b9-89d0-88d5fc896660",
  "group_name": "Huoju在Rum上说了啥",
  "owner_pubkey": "CAISIQLdBmr7WXMFgZhsBgx5+sAAGYKGzc8Agq9kGWhDZVqRpg==",
  "consensus_type": "poa",
  "encryption_type": "public",
  "cipher_key": "90f569c9fe3cd0b66b788a8e97eb00b05c8daf47915bf552f8b3d26f7b756c45",
  "app_key": "group_timeline",
  "signature": "3046022100ae7cdccd0dad63cf25daa10023dc3f9295bc7e71488d325950d3a2e1d287c4f0022100ee7438a1074bb121585f5375129531c6196f983489b2c22cf82853b3355fb0df"
}
```

```seed
{
  "genesis_block": {
    "BlockId": "1a6c044c-48e3-4a2e-81ec-a94eebe354cd",
    "GroupId": "58256759-26af-40d9-add9-b82128d3d4f9",
    "ProducerPubKey": "CAISIQNBsHQ5IQcussfAfetOp4oAjVsHzuz5ZYOt7Krs4seI2w==",
    "Hash": "0gFJF2YDQ646BNwX9TJAqPnMSl9IRF/9Nk4ap6Cgllk=",
    "Signature": "MEQCIDQB2owi0XoY8QgwM+Bv7GCz06nRLlgDIC3KwgSAoPAiAiAH1eZYVDseV6yJw6/ZVwRDpNRqfq5EHULMadTyG2GOKA==",
    "TimeStamp": "1649991701422638600"
  },
  "group_id": "58256759-26af-40d9-add9-b82128d3d4f9",
  "group_name": "故事接龙",
  "owner_pubkey": "CAISIQNBsHQ5IQcussfAfetOp4oAjVsHzuz5ZYOt7Krs4seI2w==",
  "consensus_type": "poa",
  "encryption_type": "public",
  "cipher_key": "478081ac615bcd1d81a410e9f92cc7441ee66101fa6fb45fdeb803230fb21ef5",
  "app_key": "group_timeline",
  "signature": "3045022100c45be68239358768a84d5192052bfb29213c2fa8401f2c98a9871faf2739cb3b022027822d37c048b6528e74d27f5c52c377d013197a69f2f429ac96046582a884e9"
}
```

## 调试

### 如何删除已有账号/创建新账号？

在本地电脑  `*\AppData\Local\Google\Chrome\User Data\Default\IndexedDB` 路径下找到包含 `http_wasmapp.rumsystem.net` 的文件夹并删除。

然后重新访问  http://wasmapp.rumsystem.net/ 即可。

### 开发者工具

在浏览器的工具栏中，找到“开发者工具”并打开后，查看其 console 分页来观察 logs 。
