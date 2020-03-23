### com.ktmhows.clip.pointserver.config.database

| tyep   | file          | uri | method |
|--------|---------------|-----|--------|
| Config | MybatisConfig |     |        |

### com.ktmhows.clip.pointserver.config.exceptions

| tyep      | file                      | uri | method |
|-----------|---------------------------|-----|--------|
| Exception | BadRequestException       |     |        |
| Exception | CommonException           |     |        |
| Exception | MethodNotAllowedException |     |        |
| Exception | NotFoundException         |     |        |
| Exception | UnAuthorizedException     |     |        |

### com.ktmhows.clip.pointserver.config.mvc

| tyep   | file         | uri | method |
|--------|--------------|-----|--------|
| Config | WebMvcConfig |     |        |

### com.ktmhows.clip.pointserver.config.scheduler

| tyep   | file      | uri | method |
|--------|-----------|-----|--------|
| Config | QuartzJob |     |        |

### com.ktmhows.clip.pointserver.controllers

| tyep       | file                    | uri                         | method                       |
|------------|-------------------------|-----------------------------|------------------------------|
| Controller | BZPostBackController    | ...                         | init()                       |
|            |                         | postBackForBZScreen.do      | postBackForBZScreen(...)     |
|            |                         | postBackForBZAD.do          | postBackForBZAD(...)         |
| Controller | CLiPPointController     | getPointHistory.do          | getPointHistory(...)         |
|            |                         | getPointHistoryNew.do       | getPointHistoryNew(...)      |
|            |                         | getPoint.do                 | getPoint(...)                |
|            |                         | getPointRefresh.do          | getPointRefresh(...)         |
|            |                         | plusPoint.do                | plusPoint(...)               |
|            |                         | minusPoint.do               | minusPoint(...)              |
|            |                         | exitUser.do                 | exitUser(...)                |
|            |                         | getPlusCount.do             | getPlusCount(...)            |
| Controller | NewCLiPPointController  | /getPointHistoryNew.do      | getPointHistory(...)         |
|            |                         | /getPoint.do                | getPoint(...)                |
|            |                         | /getPoint.do                | getPoint2(...)               |
|            |                         | /getPointForOtherService.do | getPointForOtherService(...) |
|            |                         | /plusPoint.do               | plusPoint(...)               |
|            |                         | /plusPointCancel.do         | plusPointCancel(...)         |
|            |                         | /minusPoint.do              | minusPoint(...)              |
|            |                         | /minusPointCancel.do        | minusPointCancel(...)        |
|            |                         | /vipCheck.do                | vipCheck(...)                |
| Controller | ~~PointBombController~~ |                             |                              |
| Controller | sendDecrypt             | /sendDecrypt.do             | sendDecrypt(..., ...)        |
|            |                         | /sendIncrypt.do             | sendIncrypt(..., ...)        |

### com.ktmhows.clip.pointserver.handlers

| tyep      | file                             | uri | method |
|-----------|----------------------------------|-----|--------|
| Exception | GlobalControllerExceptionHandler |     |        |

### com.ktmhows.clip.pointserver.interceptors

| tyep        | file                  | uri | method |
|-------------|-----------------------|-----|--------|
| Interceptor | ControllerInterceptor |     |        |

### com.ktmhows.clip.pointserver.resources

~~clip_point_server_db_script_20160712.sql~~  
~~clip_point_server_db_script_20160823.sql~~

### com.ktmhows.clip.pointserver.resources.mappers

-	ACLInfoMapper.xml
-	BuzzVillMapper.xml
-	PointHistMapper.xml
-	PointInfoMapper.xml
-	UserInfoMapper.xml

| tyep   | file            | uri | method                     |
|--------|-----------------|-----|----------------------------|
| Mapper | ACLInfoMapper   |     | getACLInfo                 |
| Mapper | BuzzVillMapper  |     | insertBZScreenPost         |
|        |                 |     | getBZScreenPostCheck       |
|        |                 |     | insertBZADPost             |
|        |                 |     | selectBZScreenPoint        |
|        |                 |     | selectBZSEvent             |
|        |                 |     | selectBZSEventNow          |
|        |                 |     | insertBZSEvent             |
|        |                 |     | insertBZSEventNow          |
|        |                 |     | selectJoinCntEvent         |
|        |                 |     | updateBZSEventNow          |
|        |                 |     | insertBZADPostNew          |
|        |                 |     | checkBuzAdTrId             |
|        |                 |     | selectBuzAdItemValue       |
|        |                 |     | updatePointBombInfo        |
| Mapper | PointHistMapper |     | getPointHist               |
|        |                 |     | getPointHistListForChange  |
|        |                 |     | getPointHistCount          |
|        |                 |     | insertPointHist            |
|        |                 |     | insertPointHistCount       |
|        |                 |     | changePointHist            |
|        |                 |     | changePointHistCount       |
|        |                 |     | changePointHistFail        |
|        |                 |     | changePointHistCountFail   |
|        |                 |     | getDuplicateChk2           |
|        |                 |     | updatePointRouletteJoin    |
|        |                 |     | selectPointHistForCancel   |
|        |                 |     | selectPointCancelInfoChk   |
|        |                 |     | insertPointCancelInfo      |
|        |                 |     | getCheckPointHist          |
| Mapper | PointInfoMapper |     | getPointInfo               |
|        |                 |     | getTblUserCardPointCache   |
|        |                 |     | getPointInfoList           |
|        |                 |     | getNewPointInfoList        |
|        |                 |     | insertPointInfo            |
|        |                 |     | updatePointInfoForExitUser |
|        |                 |     | getPlusCount               |
|        |                 |     | removePointForExitUser     |
| Mapper | UserInfoMapper  |     | getUserInfo                |
|        |                 |     | insertUserInfo             |
|        |                 |     | insertUserInfoLog          |
|        |                 |     | updateUserInfo             |
|        |                 |     | exitUserInfo               |
|        |                 |     | exitUserFinal              |
|        |                 |     | removeUserInfo             |
|        |                 |     | selectUserCiByUserToken    |
|        |                 |     | selectUserTokenByUserCi    |
|        |                 |     | checkVipByLockScreen       |

### ~~com.ktmhows.clip.pointserver.resources.mappers.backup~~

-	~~ACLInfoMapper.xml~~
-	~~BuzzVillMapper.xml~~
-	~~PointHistMapper.xml~~
-	~~PointInfoMapper.xml~~
-	~~UserInfoMapper.xml~~

### com.ktmhows.clip.pointserver.resources.repositories

| tyep      | file                      | uri | method                       |
|-----------|---------------------------|-----|------------------------------|
| Component | CLiPPointMapperRepository |     | init()                       |
|           |                           |     | changePoint(..., ...)        |
|           |                           |     | changePointRefresh(..., ...) |
|           |                           |     | exitUser(...)                |

### com.ktmhows.clip.pointserver.secure

| tyep | file                    | uri | method          |
|------|-------------------------|-----|-----------------|
| Util | AES256CipherClip_Secure |     | AES_Encode(...) |
|      |                         |     | AES_Decode(...) |

### com.ktmhows.clip.pointserver.services

| tyep    | file              | uri | method                       |
|---------|-------------------|-----|------------------------------|
| Service | BZPostBackService |     | insertBuzzScreenPoint(...)   |
|         |                   |     | insertBuzzADPoint(...)       |
|         |                   |     | insertBuzzADPoint(...)       |
|         |                   |     | getBZScreenPostCheck(...)    |
|         |                   |     | getUserCiByUserToken(...)    |
| Service | CLiPPointService  |     | init()                       |
|         |                   |     | getUserInfo(...)             |
|         |                   |     | getPointInfoList(...)        |
|         |                   |     | getNewPointInfoList(...)     |
|         |                   |     | getPointInfo(...)            |
|         |                   |     | getPointInfo2(...)           |
|         |                   |     | getPointRefresh(...)         |
|         |                   |     | plusPoint(...)               |
|         |                   |     | minusPoint(...)              |
|         |                   |     | exitUser(...)                |
|         |                   |     | checkIP(..., ...)            |
|         |                   |     | getPlusCount(...)            |
|         |                   |     | getCurrPoint(...)            |
|         |                   |     | plusPointCancel(...)         |
|         |                   |     | minusPointCancel(...)        |
|         |                   |     | getUserCiByUserToken(...)    |
|         |                   |     | getUserTokenByUserCi(...)    |
|         |                   |     | getCustIdByUserCi(...)       |
|         |                   |     | getPointForOtherService(...) |
|         |                   |     | getUserCiByCustId(...)       |
| Service | VipLoungeService  |     | checkVip(...)                |

### com.ktmhows.clip.pointserver.utils

| tyep | file                | uri | method                                       |
|------|---------------------|-----|----------------------------------------------|
| Util | AES256CipherClip    |     | setAesKey(...)                               |
|      |                     |     | AES_Encode(...)                              |
|      |                     |     | AES_Decode(...)                              |
|      |                     |     | AES_EncodeECB(...)                           |
|      |                     |     | AES_DecodeECB(...)                           |
| Util | AES256CipherForCLiP |     | setClipAesKey(...)                           |
|      |                     |     | setDgplusAesKey(...)                         |
|      |                     |     | setAesKey(...)                               |
|      |                     |     | AES_Encode(..., ..., ...)                    |
|      |                     |     | AES_Decode(..., ..., ...)                    |
|      |                     |     | setAesMsg(...)                               |
|      |                     |     | setAesMsg(...)                               |
|      |                     |     | setAesMsgByte(...)                           |
|      |                     |     | setAesMsg(..., ...)                          |
|      |                     |     | setAesMsg(..., ...)                          |
|      |                     |     | setAesMsgByte(..., ...)                      |
|      |                     |     | getAesMsg(...)                               |
|      |                     |     | getAesMsgByte(...)                           |
|      |                     |     | getAesMsg(..., ...)                          |
|      |                     |     | getAesMsgByte(..., ...)                      |
| Util | AesEcbCryptoUtil    |     | setAesEcbKey(...)                            |
|      |                     |     | aesEncryptEcb(..., ...)                      |
|      |                     |     | aesDecryptEcb(..., ...)                      |
|      |                     |     | toHex...(byte[])                             |
|      |                     |     | hexToByteArray(...)                          |
|      |                     |     | plusReplace(...)                             |
|      |                     |     | checkPhoneNo(..., ...)                       |
|      |                     |     | encryptECB(...)                              |
|      |                     |     | decryptECB(...)                              |
| Util | ClipRequesterCode   |     | init()                                       |
|      |                     |     | getName(String)                              |
| Util | ConvertUtil         |     | castint(...)                                 |
|      |                     |     | castInteger(...)                             |
|      |                     |     | castlong(...)                                |
|      |                     |     | castLong(...)                                |
|      |                     |     | castfloat(...)                               |
|      |                     |     | castFloat(...)                               |
|      |                     |     | castdouble(...)                              |
|      |                     |     | castDouble(...)                              |
|      |                     |     | castBigDecimal(...)                          |
|      |                     |     | castString(...)                              |
|      |                     |     | castDate(...)                                |
|      |                     |     | castTime(...)                                |
|      |                     |     | castTimestamp(...)                           |
|      |                     |     | castType(..., ...)                           |
|      |                     |     | convertLong2IP(...)                          |
|      |                     |     | convertIP2Long(...)                          |
|      |                     |     | convertEng2Kor(...)                          |
|      |                     |     | convertKor2Eng(...)                          |
|      |                     |     | convertPercent(...)                          |
|      |                     |     | convertPercent(...)                          |
|      |                     |     | convertString2Timestamp(...)                 |
|      |                     |     | convertWonMoney2Language(..., ..., ..., ...) |
|      |                     |     | convertNumeral2Korean(...)                   |
|      |                     |     | convertBaseMonetary2Korean(...)              |
|      |                     |     | convertNumeral2Chinese(...)                  |
|      |                     |     | convertBaseMonetary2Chinese(...)             |
|      |                     |     | convertNumeral2English(...)                  |
|      |                     |     | convertBaseMonetary2English(...)             |
|      |                     |     | convertTeenMonetary2English(...)             |
|      |                     |     | convertDecadeMonetary2English(...)           |
|      |                     |     | format(..., ...)                             |
|      |                     |     | formatDate(..., ...)                         |
|      |                     |     | formatDate(...)                              |
|      |                     |     | formatDate(..., ...)                         |
|      |                     |     | formatValidDate(...)                         |
|      |                     |     | formatValidDate(..., ...)                    |
|      |                     |     | formatTimestamp(..., ..., ...)               |
|      |                     |     | formatDollarSymbol(...)                      |
|      |                     |     | formatDollarSymbol(...)                      |
|      |                     |     | formatNumber(..., ..., ...)                  |
|      |                     |     | formatPhoneNo(..., ..., ..., ...)            |
|      |                     |     | formatWonSymbol(...)                         |
|      |                     |     | formatWonSymbol(...)                         |
|      |                     |     | justify(..., ..., ...)                       |
|      |                     |     | NVL(...)                                     |
|      |                     |     | NVL(..., ...)                                |
|      |                     |     | NVL(..., ...)                                |
|      |                     |     | NVL(..., ...)                                |
|      |                     |     | formatWonWithComma(..., ...)                 |
|      |                     |     | convertRequiredMsg(...)                      |
| Util | DateUtil            |     | getDate(...)                                 |
|      |                     |     | getTime(...)                                 |
|      |                     |     | getDate(..., ...)                            |
|      |                     |     | getLimitEndDate(..., ...)                    |
|      |                     |     | convertFormat(...)                           |
|      |                     |     | convertFormat(..., ...)                      |
|      |                     |     | convertToString(..., ...)                    |
|      |                     |     | convertToString(..., ..., ...)               |
|      |                     |     | convertToTimestamp(...)                      |
|      |                     |     | getCurrnetTimeFormattedStr(...)              |
|      |                     |     | addDays(..., ...)                            |
|      |                     |     | addDays(..., ..., ...)                       |
|      |                     |     | addMonths(..., ...)                          |
|      |                     |     | addMonths(..., ..., ...)                     |
|      |                     |     | addYears(..., ...)                           |
|      |                     |     | addYears(..., ..., ...)                      |
|      |                     |     | getCurrentTimeString()                       |
|      |                     |     | getCurrentTimeStamp()                        |
|      |                     |     | getCurrentDateString()                       |
|      |                     |     | getCurrentDateString(...)                    |
|      |                     |     | getWhichDay(...)                             |
|      |                     |     | getWhichDayNm(...)                           |
|      |                     |     | getWhichDay(..., ...)                        |
|      |                     |     | isValidDate(...)                             |
|      |                     |     | isValidDate(..., ...)                        |
|      |                     |     | getDaysBetween(..., ...)                     |
|      |                     |     | getDaysBetween(..., ..., ...)                |
|      |                     |     | getMonthsBetween(..., ...)                   |
|      |                     |     | getMonthsBetween(..., ..., ...)              |
|      |                     |     | getYearsBetween(..., ...)                    |
|      |                     |     | getYearsBetween(..., ..., ...)               |
|      |                     |     | subtractYears(..., ...)                      |
|      |                     |     | subtractYears(..., ..., ...)                 |
|      |                     |     | getLastDayOfMonth(...)                       |
|      |                     |     | getLastDayOfMonth(..., ...)                  |
|      |                     |     | getLastDay(..., ...)                         |
|      |                     |     | getElapsedTime(..., ..., ...)                |
|      |                     |     | getCurrentTime()                             |
|      |                     |     | calculateDays(..., ...)                      |
|      |                     |     | getMonthAgoDate(...)                         |
|      |                     |     | getMonthAfterDate(...)                       |
|      |                     |     | convertToString(..., ...)                    |
| Util | FileProperties      |     | FileProperties(File)                         |
|      |                     |     | FileProperties(String)                       |
|      |                     |     | getProperty(String)                          |
|      |                     |     | getProperty(String, String)                  |
|      |                     |     | propertyNames()                              |
|      |                     |     | setProperty(String, String)                  |
|      |                     |     | store(OutputStream, String)                  |
|      |                     |     | print()                                      |
| Util | HmacCrypto          |     | setHmacKey(String)                           |
|      |                     |     | getHmacVal(String)                           |
|      |                     |     | getHmacVal(String, String)                   |
|      |                     |     | bytesToHex(byte[])                           |
| Util | HttpNetwork         |     | init()                                       |
|      |                     |     | strGetUserCi(String)                         |
|      |                     |     | sendPush(PointInfoVo, UserInfoVo)            |
| Util | HttpNetworkHTTPS    |     | init()                                       |
|      |                     |     | strGetUserCi(String)                         |
|      |                     |     | sendPush(PointInfoVo, UserInfoVo)            |

### com.ktmhows.clip.pointserver.vo

| tyep | file            | uri | method |
|------|-----------------|-----|--------|
| VO   | ACLInfoVo       |     |        |
| VO   | BuzzAdItem      |     |        |
| VO   | BuzzAdNewVo     |     |        |
| VO   | BuzzVillVo      |     |        |
| VO   | BzscreenEventVo |     |        |
| VO   | PointHistVo     |     |        |
| VO   | PointInfoVo     |     |        |
| VO   | UserInfoVo      |     |        |
