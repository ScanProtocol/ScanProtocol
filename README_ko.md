# ScanProtocol
서로 다른 지갑 간의 스캔 코드 전송을 달성하기 위해 각 지갑에서 공동으로 개발 한 범용 스캔 코드 전송 계약


## EOS계열 전송 

```javascript
{
    protocol: 'ScanProtocol', 
    action: 'transfer',
    address: 'wangruixiwww',  // 전송 대상 주소
    contract: 'eosio.token',  // 토큰을 선택 혹은 지정하거나 지갑의 코드를 스캔하여 전송 토큰을 선택할 수 있습니다. 필드 symbol와 precision을 일치시켜야합니다.
    symbol: 'EOS',  // 토큰을 선택 혹은 지정하거나 지갑의 코드를 스캔하여 전송 토큰을 선택할 수 있습니다. 필드contract와 precision을 일치시켜야합니다.
    precision: 4,  // 토큰을 선택 혹은 지정하거나 지갑의 코드를 스캔하여 전송 토큰을 선택할 수 있습니다. 필드 contract와 symbol를 일치시켜야합니다.

    blockchain: 'EOS', // BTC, ETH, EOS, BOS, MEET.ONE 
    amount: '2.4', // 진실한 전송 수 선택 가능
    memo: 'something to say', // 메모 선택 가능
    chainid:  'd5a3d18fbb3c084e3b1f3fa98c21014b5f3db536cc15d08f9f6479517c6a3d86' // 선택 가능
}

```

## ETH 전송

```javascript
{
    protocol: 'ScanProtocol', 
    action: 'transfer',
    address: '0x4e9ce36e442e55ecd9025b9a6e0d88485d628a67',  // 전송 대상 주소
    contract: '0xB8c77482e45F1F44dE1745F52C74426C631bDD52', // ETH비움 또는 비어 있음
    symbol: 'BNB',
    decimal: 18,
    blockchain: 'ETH',
    amount: '2.4' // 진실한 전송 수 선택 가능
}
```

## 일반적으로 쓰이는 필드 
 • 후속 보충된 기타 퍼블릭 체인, 최대한 일관성을 유지
```javascript
{
    protocol: 'ScanProtocol', 
    action: 'transfer',
    address: '', 
    contract: '',
    symbol: '',
    blockchain: '',
    amount: '' // 진실한 전송 수 선택 가능
}
```

## 오프라인 지불
```javascript
{
  "protocol":"pay",
  "name":"西贝莜面村",
  "chain":"BOS"
  "contract":"eosio.token",  //선택 과목
  "address":"accountuser",
  "symbol":"BOS",
  "memo":"",    //선택 과목
  "amount":"10"  //선택 과목   
}
```