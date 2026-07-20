# List Objects with Wasabi

Retrieves objects from a specific bucket in Wasabi.

## Endpoint

- **Method:** `GET`
- **Path:** `/:bucketName`
- **Base URL:** `https://s3.wasabisys.com`
- **Official documentation:** [List Objects](https://docs.aws.amazon.com/AmazonS3/latest/API/API_ListObjects.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `bucketName` | path | `string` | yes | Name of the bucket to list objects from. |
