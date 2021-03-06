# JLExtension

## 如何安装

### 1 手动安装 

step1:将项目JLExtension/Source 文件夹中的文件直接拖入你的项目中即可

step2:导入.h文件

#import "JLExtension.h"

### 2 CocoaPods 

step1: add the following line to your Podfile:

pod 'JLExtension','~> 0.0.1'

step2: 导入.h文件

#import <JLExtension/JLExtension.h>

## 使用示例

## 代码说明

### NSDictionary
```
@interface NSDictionary (Extension)

/**
 从字典中取出一个字典

 @param key 关键字
 @return 关键字存在时返回实际的值，不存在时返回@{}
 */
- (NSDictionary *)dictionaryForKey:(NSString *)key;

/**
 从字典中取出一个数组

 @param key 关键字
 @return 关键字存在时返回实际的值，不存在时返回@[]
 */
- (NSArray *)arrayForKey:(NSString *)key;

/**
 从字典中取出一个字符串
 
 @param key 关键字
 @return 关键字存在时返回实际的值，不存在时返回@""
 */
- (NSString *)stringForKey:(NSString *)key;

/**
 从字典中取出一个布尔值
 
 @param key 关键字
 @return 关键字存在时，如果实际的值是为0或@"0"返回NO，其他值返回YES，不存在时直接返回NO
 */
- (BOOL)boolForKey:(NSString *)key;

/**
 从字典中取出一个整型数字
 
 @param key 关键字
 @return 关键字存在时返回实际的值，不存在时返回0
 */
- (NSInteger)intForKey:(NSString *)key;

/**
 从字典中取出一个双精度型数字
 
 @param key 关键字
 @return 关键字存在时返回实际的值，不存在时返回0.00
 */
- (double)doubleForKey:(NSString *)key;

@end
```

### NSArray
```
@interface NSArray (Extension)

/**
 从数组中取出一个整数型数字
 
 @param index 序列号
 @return 序列号在数组范围时返回实际的值，不存在时返回0
 */
- (NSInteger)intAtIndex:(NSUInteger)index;

/**
 从数组中取出一个双精度型数字
 
 @param index 序列号
 @return 序列号在数组范围时返回实际的值，不存在时返回0.00
 */
- (double)doubleAtIndex:(NSUInteger)index;

/**
 从数组中取出一个字典
 
 @param index 序列号
 @return 序列号在数组范围时返回实际的值，不存在时返回@{}
 */
- (NSDictionary *)dictionaryAtIndex:(NSUInteger)index;

/**
 从数组中取出一个数组
 
 @param index 序列号
 @return 序列号在数组范围时返回实际的值，不存在时返回@[]
 */
- (NSDictionary *)arrayAtIndex:(NSUInteger)index;

/**
 从数组中取出一个字符串
 
 @param index 序列号
 @return 序列号在数组范围时返回实际的值，不存在时返回@""
 */
- (NSString *)stringAtIndex:(NSUInteger)index;

- (NSString *)RMBAtIndex:(NSUInteger)index;
@end
```

### NSString
```
@interface NSString (Extension)

/**
 MD5加密

 @return MD5加密值
 */
- (NSString *)md5Encrypt;

/**
 DES字符串加密

 @param key 密钥 64位
 @return 字符串密文
 */
- (NSString *)desEncryptWithKey:(NSString *)key;

/**
 DES字符串解密

 @param key 密钥 64位
 @return 字符串明文
 */
- (NSString *)desDecryptWithKey:(NSString*)key;

/**
 AES256字符串加密

 @param key 密钥 64位
 @return 字符串密文
 */
- (NSString *)aes256EncryptWithKey:(NSString *)key;

/**
 AES256字符串解密

 @param key 密钥 64位
 @return 字符串明文
 */
- (NSString *)aes256DecryptWithKey:(NSString *)key;

/**
 Base64的字符串转换为图片

 @return UIImage
 */
- (UIImage *)base64ToUIImage;

/**
 计算字符串字节长度，中文2个字节，英文1个字节

 @return 计算字符串字节长度
 */
- (NSUInteger)textLength;

/**
 将十六进制颜色值转换为UIColor颜色

 @return UIColor
 */
- (UIColor *)hexStringToColor;
@end
```
