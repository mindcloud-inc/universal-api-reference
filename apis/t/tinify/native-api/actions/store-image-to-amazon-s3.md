# Store Image To Amazon S3 with Tinify

Stores an optimized image from Tinify in Amazon S3.

## Endpoint

- **Method:** `POST`
- **Path:** `/output/:outputId`
- **Base URL:** `https://api.tinify.com`
- **Official documentation:** [Store Image To Amazon S3](https://tinify.com/developers/reference/http#saving-to-amazon-s3)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `outputId` | path | `string` | yes | Tinify output identifier from a prior compression URL. |
| `store.aws_access_key_id` | body | `string` | yes | AWS access key ID with permission to put objects at the target path. |
| `store.aws_secret_access_key` | body | `string` | yes | AWS secret access key for the S3 user. |
| `store.region` | body | `string` | yes | AWS region for the S3 bucket, such as us-west-1. |
| `store.path` | body | `string` | yes | Destination path in the format bucket/path/filename. |
