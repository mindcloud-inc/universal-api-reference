# Store File From URL with Filestack

Creates a new file in Filestack from a URL.

## Endpoint

- **Method:** `POST`
- **Path:** `/store/S3`
- **Base URL:** `https://www.filestackapi.com/api`
- **Official documentation:** [Store File From URL](https://www.filestack.com/docs/api/file/#store)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `filename` | query | `string` | no | Optional filename to store in Filestack. |
| `mimetype` | query | `string` | no | Optional MIME type override, for example image/png. |
| `url` | body | `string` | yes | Public URL of the file to import into Filestack. |
