# Connect File with Tako

Connects a file to Tako for analysis.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/beta/file_connector`
- **Base URL:** `https://tako.com/api`
- **Official documentation:** [Connect File](https://docs.tako.com/api-reference/file-connector)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `display_name` | body | `string` | no | Optional file name to show inside Tako. |
| `file_url` | body | `string` | yes | Publicly reachable URL that Tako should download and connect. |
