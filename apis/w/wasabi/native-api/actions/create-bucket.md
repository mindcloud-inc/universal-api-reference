# Create Bucket with Wasabi

Creates a new bucket in Wasabi.

## Endpoint

- **Method:** `PUT`
- **Path:** `/:name`
- **Base URL:** `https://s3.wasabisys.com`
- **Official documentation:** [Create Bucket](https://docs.aws.amazon.com/AmazonS3/latest/API/API_CreateBucket.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | path | `string` | yes | Globally unique DNS-compatible bucket name. |
