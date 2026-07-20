# Search Sharees with Next Cloud OCS

Finds sharees in Next Cloud OCS.

## Endpoint

- **Method:** `GET`
- **Path:** `/ocs/v1.php/apps/files_sharing/api/v1/sharees`
- **Base URL:** `https://demo2.nextcloud.com`
- **Official documentation:** [Search Sharees](https://docs.nextcloud.com/server/latest/developer_manual/client_apis/OCS/ocs-sharee-api.html#search-sharees)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `search` | query | `string` | yes | Search term for sharee lookup. |
