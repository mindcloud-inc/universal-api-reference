# Wasabi: Native API Reference

A consolidated summary of Wasabi's API configuration and 3 documented operations, with links to official documentation.

- **Official docs:** https://docs.wasabi.com/apidocs/wasabi-api
- **API base URL:** `https://s3.wasabisys.com`

## Authentication

### S3 Access Key

Use a Wasabi S3 access key pair. Requests require AWS Signature Version 4-compatible signing.

### Credentials

- **Access Key ID:** `accessKeyId` · required · Wasabi S3 Access Key ID generated in the Wasabi Console.
- **Secret Access Key:** `secretAccessKey` · required · Wasabi S3 Secret Access Key shown once when the access key is generated.
- **S3 Endpoint:** `s3Endpoint` · required · Wasabi S3 endpoint URL, for example https://s3.wasabisys.com.
- **Region:** `region` · required · Wasabi storage region used for AWS Signature Version 4 signing.

[Official authentication documentation](https://docs.wasabi.com/apidocs/authentication-with-s3-api)

## API conventions

Request bodies use XML.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/xml` |

Responses from this API use XML.

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 1000 ms before the first retry. Stop after 2 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (3 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Bucket](actions/create-bucket.md) | `PUT /:name` | [docs](https://docs.aws.amazon.com/AmazonS3/latest/API/API_CreateBucket.html) |
| [List Buckets](actions/list-buckets.md) | `GET /` | [docs](https://docs.aws.amazon.com/AmazonS3/latest/API/API_ListBuckets.html) |
| [List Objects](actions/list-objects.md) | `GET /:bucketName` | [docs](https://docs.aws.amazon.com/AmazonS3/latest/API/API_ListObjects.html) |
