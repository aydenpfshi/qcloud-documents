## 概述
通过 DescribeKey 查看指定 CMK 的详细信息，信息包括用户主密钥 CMK 名称、ID、状态、所属地区等密钥详情。

本文示例使用腾讯云 [命令行工具 TCCLI](https://cloud.tencent.com/product/cli)，后续您可以使用任何搜支持的编程语言调用。该 API 操作的 KeyId 为必选参数，您可以查看 [DescribeKey](https://cloud.tencent.com/document/product/573/34428) 接口文档来查看其它参数说明。

## 示例
查看指定 CMK 详细信息。

#### 输入示例
```shell
tccli kms DescribeKey --region ap-guangzhou --KeyId 521xxxxx-xxxx-xxxx-xxxx-52xxxxd4
```



#### 输出示例
在 API 成功执行的情况下，将返回 CMK 的详细信息。
```shell
{
    "KeyMetadata": {
        "KeyId": "521xxxxx-xxxx-xxxx-xxxx-52xxxxd",
        "Description": "this is test for gz key",
        "CreatorUin": Mosaic,
        "KeyRotationEnabled": false,
        "NextRotateTime": Mosaic,
        "CreateTime": Mosaic,
        "Alias": "d-test-gz01",
        "KeyUsage": "ENCRYPT_DECRYPT",
        "DeletionDate": 0,
        "KeyState": "Enabled",
        "Type": 4,
        "Owner": "Mosaic"
    },
    "RequestId": "Mosaic"
}

```
