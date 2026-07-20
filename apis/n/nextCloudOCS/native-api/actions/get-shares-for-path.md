# Get Shares For Path with Next Cloud OCS

Retrieves shares for a path from Next Cloud OCS.

## Endpoint

- **Method:** `GET`
- **Path:** `/ocs/v2.php/apps/files_sharing/api/v1/shares`
- **Base URL:** `https://demo2.nextcloud.com`
- **Official documentation:** [Get Shares For Path](https://docs.nextcloud.com/server/latest/developer_manual/client_apis/OCS/ocs-share-api.html#get-shares-from-a-specific-file-or-folder)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `path` | query | `string` | yes | Path to the file or folder. |
