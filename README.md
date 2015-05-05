# UpdateCheck
when you publish new version android app,maybe you want all your application user update new version.

this process follow 4-steps:
1. check googleplay app version
2. check device app version
3. compare version
4. alert new version update!

## How to use
1. check googleplay app version
```java
  String store_version = MarketVersionChecker.getMarketVersion(getPackageName());
```
2. check device app version
```java
  String device_version = getPackageManager().getPackageInfo(getPackageName(), 0).versionName;
```

3. compare version
```java
  if (store_version.compareTo(device_version) > 0) {
						// need update

					} else {
						// no need update

					}
```



## Reference
* [`getMarketVersion()`](http://www.androidside.com/bbs/board.php?bo_table=B56&wr_id=24663)
* [`getMarketVersionFast()`](http://www.androidside.com/bbs/board.php?bo_table=B49&wr_id=135849)
