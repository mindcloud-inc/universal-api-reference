# Create Direct Download Link with Next Cloud OCS

Creates a new direct download link in Next Cloud OCS.

## Endpoint

- **Method:** `POST`
- **Path:** `/ocs/v2.php/apps/dav/api/v1/direct`
- **Base URL:** `https://demo2.nextcloud.com`
- **Official documentation:** [Create Direct Download Link](https://docs.nextcloud.com/server/latest/developer_manual/client_apis/OCS/ocs-api-overview.html#direct-download)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `fileId` | body | `string` | yes | Nextcloud file ID for the direct download link. |
