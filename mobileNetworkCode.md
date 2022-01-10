## bug
机型：iPhone 12 Pro Max
系统：iOS 15.1
运营商：联通卡
问题：
```objective-c
CTTelephonyNetworkInfo *info = [[CTTelephonyNetworkInfo alloc]init];
CTCarrier *carrier = [info subscriberCellularProvider];
NSString * mcc = [carrier mobileCountryCode];
NSString * mnc = [carrier mobileNetworkCode];
//mcc 和 mnc 都为nil    carrierName 有值
```

解释：
官方解释只有两种情况下返回nil
- sim卡未插
- 插入的sim卡不在服务区

显然是个bug