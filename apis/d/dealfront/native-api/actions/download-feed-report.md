# Download Feed Report with Dealfront

Retrieves a feed report from Dealfront.

## Endpoint

- **Method:** `GET`
- **Path:** `/download/:download_file_name`
- **Base URL:** `https://api.leadfeeder.com`
- **Official documentation:** [Download Feed Report](https://docs.leadfeeder.com/api/#downloading-the-report)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `download_file_name` | path | `string` | yes | File name portion from the download_url returned by the export status response. |
