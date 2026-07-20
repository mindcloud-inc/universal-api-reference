# Store Image To Amazon S3 with TinyPNG

Stores a TinyPNG image in Amazon S3.

## Endpoint

- **Method:** `POST`
- **Path:** `{{outputPath}}`
- **Base URL:** `https://api.tinify.com`
- **Official documentation:** [Store Image To Amazon S3](https://tinify.com/developers/reference/http#saving-to-amazon-s3)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `outputPath` | path | `string` | yes | TinyPNG output path returned by a previous action, for example `/output/abc123`. |
| `store.aws_access_key_id` | body | `string` | yes | AWS access key ID used to upload the object. |
| `store.aws_secret_access_key` | body | `string` | yes | AWS secret access key used to upload the object. |
| `store.region` | body | `string` | yes | AWS region where the destination bucket is located. |
| `store.path` | body | `string` | yes | Destination path in the format <bucket>/<path>/<filename>. |
| `store.headers.Cache-Control` | body | `string` | no | Optional Cache-Control header value to apply on the stored object. |
