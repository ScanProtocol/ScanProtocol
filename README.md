# ScanProtocol
一个通用扫码转账协议，由各钱包共同制定，旨在实现不同钱包间扫码转账


## EOS系 转账

```javascript
{
  protocol: '一个固定的响亮的名字', 
  action: 'transfer',
  address: 'wangruixiwww', 
  contract: 'eosio.token',
  symbol: 'EOS',
  precision: 4,
  blockchain: 'EOS', // BTC, ETH, EOS, BOS, MEETONE 
  amount: '2.4', // 可选  真实转账数量
  memo: 'something to say', // 可选 备注信息
  chainid: 'd5a3d18fbb3c084e3b1f3fa98c21014b5f3db536cc15d08f9f6479517c6a3d86' // 可选 
}
```

## ETH 转账

```javascript
{
  protocol: '一个固定的响亮的名字', 
  action: 'transfer',
  address: '0x4e9ce36e442e55ecd9025b9a6e0d88485d628a67', 
  contract: '0xB8c77482e45F1F44dE1745F52C74426C631bDD52', // ETH不填或为空
  symbol: 'BNB',
  decimal: 18,
  blockchain: 'ETH',
  amount: '2.4' // 可选  真实转账数量
}
```




## 比较通用字段
- 后续补充的其他公链,尽量保持一致性
```javascript
{
  protocol: '一个固定的响亮的名字', 
  action: 'transfer',
  address: '', 
  contract: '',
  symbol: '',
  blockchain: '',
  amount: '' // 可选  真实转账数量
}
```




