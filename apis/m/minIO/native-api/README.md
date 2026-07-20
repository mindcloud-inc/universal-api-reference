# MinIO: Native API Reference

A consolidated summary of MinIO's API configuration and 30 documented operations, with links to official documentation.

- **Official docs:** https://docs.min.io/community/minio-object-store/
- **API base URL:** `{baseApiUrl}`

## Authentication

### Access Key + Secret Key

Connect to MinIO using an access key, secret key, and MinIO endpoint URLs.

### Credentials

- **API Key:** `apiKey` · required
- **Base API URL:** `baseApiUrl` · required · Base S3-compatible HTTPS endpoint, for example https://play.min.io:9000.
- **Secret Key:** `secretKey` · required · Secret key paired with the MinIO access key.
- **Console URL:** `consoleUrl` · required · Console URL used for human-facing bucket and object links, for example https://play.min.io.

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://docs.min.io/enterprise/aistor-object-store/developers/sdk/python/)

## Pagination

Use `max-keys` in the query string to set the page size (default 1000; accepted range 1–1000). Use `continuation-token` in the query string as the pagination cursor.

## Endpoints (30 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Copy Object](actions/copy-object.md) | `PUT /:bucket/:key` | [docs](https://docs.aws.amazon.com/AmazonS3/latest/API/API_CopyObject.html) |
| [Create Bucket](actions/create-bucket.md) | `PUT /:bucket` | [docs](https://docs.aws.amazon.com/AmazonS3/latest/API/API_CreateBucket.html) |
| [Delete Bucket](actions/delete-bucket.md) | `DELETE /:bucket` | [docs](https://docs.aws.amazon.com/AmazonS3/latest/API/API_DeleteBucket.html) |
| [Delete Bucket CORS](actions/delete-bucket-cors.md) | `DELETE /:bucket` | [docs](https://docs.aws.amazon.com/AmazonS3/latest/API/API_DeleteBucketCors.html) |
| [Delete Bucket Lifecycle](actions/delete-bucket-lifecycle.md) | `DELETE /:bucket` | [docs](https://docs.aws.amazon.com/AmazonS3/latest/API/API_DeleteBucketLifecycle.html) |
| [Delete Bucket Policy](actions/delete-bucket-policy.md) | `DELETE /:bucket` | [docs](https://docs.aws.amazon.com/AmazonS3/latest/API/API_DeleteBucketPolicy.html) |
| [Delete Bucket Tagging](actions/delete-bucket-tagging.md) | `DELETE /:bucket` | [docs](https://docs.aws.amazon.com/AmazonS3/latest/API/API_DeleteBucketTagging.html) |
| [Delete Object](actions/delete-object.md) | `DELETE /:bucket/:key` | [docs](https://docs.aws.amazon.com/AmazonS3/latest/API/API_DeleteObject.html) |
| [Delete Object Tagging](actions/delete-object-tagging.md) | `DELETE /:bucket/:key` | [docs](https://docs.aws.amazon.com/AmazonS3/latest/API/API_DeleteObjectTagging.html) |
| [Delete Objects](actions/delete-objects.md) | `POST /:bucket` | [docs](https://docs.aws.amazon.com/AmazonS3/latest/API/API_DeleteObjects.html) |
| [Get Bucket Encryption](actions/get-bucket-encryption.md) | `GET /:bucket` | [docs](https://docs.aws.amazon.com/AmazonS3/latest/API/API_GetBucketEncryption.html) |
| [Get Bucket Lifecycle Configuration](actions/get-bucket-lifecycle-configuration.md) | `GET /:bucket` | [docs](https://docs.aws.amazon.com/AmazonS3/latest/API/API_GetBucketLifecycleConfiguration.html) |
| [Get Bucket Location](actions/get-bucket-location.md) | `GET /:bucket` | [docs](https://docs.aws.amazon.com/AmazonS3/latest/API/API_GetBucketLocation.html) |
| [Get Bucket Policy](actions/get-bucket-policy.md) | `GET /:bucket` | [docs](https://docs.aws.amazon.com/AmazonS3/latest/API/API_GetBucketPolicy.html) |
| [Get Bucket Tagging](actions/get-bucket-tagging.md) | `GET /:bucket` | [docs](https://docs.aws.amazon.com/AmazonS3/latest/API/API_GetBucketTagging.html) |
| [Get Bucket Versioning](actions/get-bucket-versioning.md) | `GET /:bucket` | [docs](https://docs.aws.amazon.com/AmazonS3/latest/API/API_GetBucketVersioning.html) |
| [Get Object](actions/get-object.md) | `GET /:bucket/:key` | [docs](https://docs.aws.amazon.com/AmazonS3/latest/API/API_GetObject.html) |
| [Get Object Attributes](actions/get-object-attributes.md) | `GET /:bucket/:key` | [docs](https://docs.aws.amazon.com/AmazonS3/latest/API/API_GetObjectAttributes.html) |
| [Get Object Tagging](actions/get-object-tagging.md) | `GET /:bucket/:key` | [docs](https://docs.aws.amazon.com/AmazonS3/latest/API/API_GetObjectTagging.html) |
| [List Buckets](actions/list-buckets.md) | `GET /` | [docs](https://docs.aws.amazon.com/AmazonS3/latest/API/API_ListBuckets.html) |
| [List Object Versions](actions/list-object-versions.md) | `GET /:bucket` | [docs](https://docs.aws.amazon.com/AmazonS3/latest/API/API_ListObjectVersions.html) |
| [List Objects](actions/list-objects.md) | `GET /:bucket` | [docs](https://docs.aws.amazon.com/AmazonS3/latest/API/API_ListObjects.html) |
| [List Objects V2](actions/list-objects-v2.md) | `GET /:bucket` | [docs](https://docs.aws.amazon.com/AmazonS3/latest/API/API_ListObjectsV2.html) |
| [Put Bucket CORS](actions/put-bucket-cors.md) | `PUT /:bucket` | [docs](https://docs.aws.amazon.com/AmazonS3/latest/API/API_PutBucketCors.html) |
| [Put Bucket Lifecycle Configuration](actions/put-bucket-lifecycle-configuration.md) | `PUT /:bucket` | [docs](https://docs.aws.amazon.com/AmazonS3/latest/API/API_PutBucketLifecycleConfiguration.html) |
| [Put Bucket Policy](actions/put-bucket-policy.md) | `PUT /:bucket` | [docs](https://docs.aws.amazon.com/AmazonS3/latest/API/API_PutBucketPolicy.html) |
| [Put Bucket Tagging](actions/put-bucket-tagging.md) | `PUT /:bucket` | [docs](https://docs.aws.amazon.com/AmazonS3/latest/API/API_PutBucketTagging.html) |
| [Put Bucket Versioning](actions/put-bucket-versioning.md) | `PUT /:bucket` | [docs](https://docs.aws.amazon.com/AmazonS3/latest/API/API_PutBucketVersioning.html) |
| [Put Object](actions/put-object.md) | `PUT /:bucket/:key` | [docs](https://docs.aws.amazon.com/AmazonS3/latest/API/API_PutObject.html) |
| [Put Object Tagging](actions/put-object-tagging.md) | `PUT /:bucket/:key` | [docs](https://docs.aws.amazon.com/AmazonS3/latest/API/API_PutObjectTagging.html) |
