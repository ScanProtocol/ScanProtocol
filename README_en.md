# ScanProtocol
A universal scanning code transfer protocol developed by several wallet teams, aiming to achieve scanning code transfer among different wallets


## Transfer tokens on EOS

```javascript
{
  protocol: 'ScanProtocol', 
  action: 'transfer',
  address: 'wangruixiwww',  // Receiver
  contract: 'eosio.token',  // Optional, you can specify the token, or you can choose the transfer token by scanning the code with the wallet which need to match the fields symbol and precision.
  symbol: 'EOS',  // Optional, you can specify the token, or you can choose the transfer token by scanning the code with the wallet which need to match the fields symbol and precision.
  precision: 4,  // Optional, you can specify the token, or you can choose the transfer token by scanning the code with the wallet which need to match the fields symbol and precision.
  blockchain: 'EOS', // BTC, ETH, EOS, BOS, MEET.ONE 
  amount: '2.4', // Optional  Actual amount of transfer tokens
  memo: 'something to say', // Optional Memo
  chainid: 'd5a3d18fbb3c084e3b1f3fa98c21014b5f3db536cc15d08f9f6479517c6a3d86' // Optional 
}
```

## Transfer tokens on ETH

```javascript
{
  protocol: 'ScanProtocol', 
  action: 'transfer',
  address: '0x4e9ce36e442e55ecd9025b9a6e0d88485d628a67',  // Receiver
  contract: '0xB8c77482e45F1F44dE1745F52C74426C631bDD52', // ETH null or blank
  symbol: 'BNB',
  decimal: 18,
  blockchain: 'ETH',
  amount: '2.4' // Optional  Actual amount of transfer tokens
}
```

## Generic field
- Please keep the consistency of other public chains that added later
```javascript
{
  protocol: 'ScanProtocol', 
  action: 'transfer',
  address: '', 
  contract: '',
  symbol: '',
  blockchain: '',
  amount: '' // Optional  Actual amount of transfer tokens
}
```

## Offline payment

```javascript
{
  "protocol":"pay",
  "name":"西贝莜面村",
  "chain":"BOS"
  "contract":"eosio.token",  //optional
  "address":"accountuser",
  "symbol":"BOS",
  "memo":"",    //optional
  "amount":"10"  //optional   
}
```