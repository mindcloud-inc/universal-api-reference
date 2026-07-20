# List Jobs with Api2Convert

Retrieves active job records from Api2Convert.

## Endpoint

- **Method:** `GET`
- **Path:** `/jobs`
- **Base URL:** `https://api.api2convert.com/v2`
- **Official documentation:** [List Jobs](https://api.api2convert.com/v2/schema)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `status` | query | `string` | no | Filter jobs by status code. |
| `page` | query | `string` | no | Page number for paginated job results. |
