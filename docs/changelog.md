# Changelog
All notable changes to this project will be documented in this file.

## [v0.0.5]- 2020-03-20
#### Added
- `KArr.InInt64Slice`
- `KArr.InIntSlice`
- `KArr.InStringSlice`
- `KArr.IsEqualArray`
- `KConv.Byte2Hexs`
- `KConv.Hexs2Byte`
- `KConv.Runes2Bytes`
- `KEncr.AesCBCDecrypt`
- `KEncr.AesCBCEncrypt`
- `KEncr.AesCFBDecrypt`
- `KEncr.AesCFBEncrypt`
- `KEncr.AesCTRDecrypt`
- `KEncr.AesCTREncrypt`
- `KEncr.AesOFBDecrypt`
- `KEncr.AesOFBEncrypt`
- `KEncr.GenerateRsaKeys`
- `KEncr.RsaPrivateDecrypt`
- `KEncr.RsaPrivateEncrypt`
- `KEncr.RsaPublicDecrypt`
- `KEncr.RsaPublicEncrypt`
- `KFile.AppendFile`
- `KFile.GetFileMode`
- `KFile.ReadFirstLine`
- `KFile.ReadLastLine`
- `KNum.Percent`
- `KNum.RoundPlus`
- `KOS.GetBiosInfo`
- `KOS.GetBoardInfo`
- `KOS.GetCpuInfo`
- `KOS.IsProcessExists`
- `KStr.AtWho`
- `KStr.ClearUrlPrefix`
- `KStr.ClearUrlSuffix`
- `KStr.Gravatar`
- `KStr.IsWord`
- `KStr.RemoveEmoji`
- `KStr.UuidV4`
- `KTime.DaysBetween`
- `KTime.EndOfDay`
- `KTime.EndOfMonth`
- `KTime.EndOfWeek`
- `KTime.EndOfYear`
- `KTime.StartOfDay`
- `KTime.StartOfMonth`
- `KTime.StartOfWeek`
- `KTime.StartOfYear`

#### Fixed
- none

#### Changed
- `KFile.IsFile` 增加文件类型参数LkkFileType
- `KFile.WriteFile` 增加权限参数perm
- `KOS.Getenv` 增加默认值参数
- `KStr.Random` 移除time.Sleep
- `KTime.GetMonthDays` 放弃map,直接比较
- rename `KOS.GetProcessExeByPid` to `KOS.GetProcessExecPath`
- rename `KTime.Time` to `KTime.UnixTime`

#### Removed
- none

## [v0.0.4]- 2020-03-06
#### Added
- `KStr.Index`
- `KStr.LastIndex`

#### Fixed
- none

#### Changed
- `KStr.RemoveBefore` 增加参数ignoreCase
- `KStr.RemoveAfter` 增加参数ignoreCase
- `KStr.StartsWith` 增加参数ignoreCase,使用Index代替MbSubstr
- `KStr.EndsWith` 增加参数ignoreCase,使用LastIndex代替MbSubstr

#### Removed
- none

## [v0.0.3]- 2020-03-03
#### Added
- 增加常量`DYNAMIC_KEY_LEN`动态密钥长度

#### Fixed
- `KEncr.AuthCode` 修复bounds out of range错误

#### Changed
- `KEncr.AuthCode` 动态密钥长度改为8
- `KEncr.EasyEncrypt` 动态密钥长度改为8
- `KEncr.EasyDecrypt` 动态密钥长度改为8
- `KTime.CheckDate(month, day, year int)` to `CheckDate(year, month, day int)`
- `KNum.ByteFormat` 增加'delimiter'参数,为数字和单位间的分隔符

#### Removed
- none

## [v0.0.2]- 2020-02-09
#### Added
- `KArr.JoinInts`
- `KArr.JoinStrings`
- `KArr.Unique64Ints`
- `KArr.UniqueInts`
- `KArr.UniqueStrings`
- `KConv.ToBool`
- `KConv.IsNil`
- `KDbug.CallMethod`
- `KDbug.GetFuncDir`
- `KDbug.GetFuncFile`
- `KDbug.GetFuncPackage`
- `KDbug.GetMethod`
- `KDbug.HasMethod`
- `KFile.CountLines`
- `KFile.IsZip`
- `KFile.ReadInArray`
- `KFile.UnZip`
- `KFile.Zip`
- `KNum.Average`
- `KNum.AverageFloat64`
- `KNum.AverageInt`
- `KNum.FloatEqual`
- `KNum.GeoDistance`
- `KNum.MaxFloat64`
- `KNum.MaxInt`
- `KNum.RandFloat64`
- `KNum.RandInt64`
- `KNum:Sum`
- `KNum:SumFloat64`
- `KNum:SumInt`
- `KOS.ForceGC`
- `KOS.GetPidByPort`
- `KOS.GetProcessExeByPid`
- `KOS.TriggerGC`
- `KStr.CountWords`
- `KStr.EndsWith`
- `KStr.Img2Base64`
- `KStr.IsBlank`
- `KStr.IsEmpty`
- `KStr.IsLower`
- `KStr.IsMd5`
- `KStr.IsSha1`
- `KStr.IsSha256`
- `KStr.IsSha512`
- `KStr.IsUpper`
- `KStr.Jsonp2Json`
- `KStr.StartsWith`
- `KStr.ToKebabCase`
- `KStr.ToSnakeCase`
- `KTime.Day`
- `KTime.Hour`
- `KTime.Minute`
- `KTime.Month`
- `KTime.Second`
- `KTime.Str2Timestruct`
- `KTime.Year`

#### Fixed
- `KStr.Trim`, 当输入"0"时,结果为空的BUG.

#### Changed
- `KArr.Implode`, 增加对map的处理.
- `KEncr.EasyDecrypt`, 改进循环.
- `KEncr.EasyEncrypt`, 改进循环.
- `KNum.Max`, 接受任意类型的参数.
- `KNum.Min`, 接受任意类型的参数.
- `KNum.Sum`, 只对数值类型求和.
- `KOS.Pwd`, 弃用os.Args[0],改用os.Executable.
- `KStr.IsASCII`, 弃用正则判断.
- `KStr.IsEmail`, 去掉邮箱是否真实存在的检查.
- `KStr.MbSubstr`, 允许参数start/length为负数.
- `KStr.Substr`, 允许参数start/length为负数.
- rename `KArr.ArraySearchMutilItem` to `ArraySearchMutil`
- rename `KArr.MapMerge` to `MergeMap`
- rename `KArr.SliceMerge` to `MergeSlice`
- rename `KConv.Bin2dec` to `Bin2Dec`
- rename `KConv.Bin2hex` to `Bin2Hex`
- rename `KConv.ByteToFloat64` to `Byte2Float64`
- rename `KConv.ByteToInt64` to `Byte2Int64`
- rename `KConv.BytesSlice2Str` to `Bytes2Str`
- rename `KConv.Dec2bin` to `Dec2Bin`
- rename `KConv.Dec2hex` to `Dec2Hex`
- rename `KConv.Dec2oct` to `Dec2Oct`
- rename `KConv.Hex2bin` to `Hex2Bin`
- rename `KConv.Hex2dec` to `Hex2Dec`
- rename `KConv.Ip2long` to `Ip2Long`
- rename `KConv.Long2ip` to `Long2Ip`
- rename `KConv.Oct2dec` to `Oct2Dec`
- rename `KConv.Str2ByteSlice` to `Str2Bytes`
- rename `KConv.StrictStr2Float` to `Str2FloatStrict`
- rename `KConv.StrictStr2Int` to `Str2IntStrict`
- rename `KConv.StrictStr2Uint` to `Str2UintStrict`
- rename `KFile.Filemtime` to `GetModTime`
- rename `KFile.GetContents` to `ReadFile`
- rename `KFile.PutContents` to `WriteFile`
- rename `KStr.CamelName` to `ToCamelCase`
- rename `KStr.LowerCaseFirstWords` to `Lcwords`
- rename `KStr.StrShuffle` to `Shuffle`
- rename `KStr.Strrev` to `Reverse`
- rename `KStr.UpperCaseFirstWords` to `Ucwords`
- rename `KTime.Strtotime` to `Str2Timestamp`

#### Removed
- remove `KConv.Int2Bool`


*--end of file--*