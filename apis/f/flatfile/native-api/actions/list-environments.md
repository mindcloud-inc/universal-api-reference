# List Environments with Flatfile

Retrieves a list of environments from Flatfile.

## Endpoint

- **Method:** `GET`
- **Path:** `/environments`
- **Base URL:** `https://api.x.flatfile.com/v1`
- **Official documentation:** [List Environments](https://reference.flatfile.com/api-reference/environments/list)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `pageNumber` | query | `string` | no | Page number based on the selected page size. |
| `pageSize` | query | `string` | no | Number of environments to return in a page. |
