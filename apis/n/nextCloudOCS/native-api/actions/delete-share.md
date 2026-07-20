# Delete Share with Next Cloud OCS

Deletes a share from Next Cloud OCS.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/ocs/v2.php/apps/files_sharing/api/v1/shares/{{shareId}}`
- **Base URL:** `https://demo2.nextcloud.com`
- **Official documentation:** [Delete Share](https://docs.nextcloud.com/server/latest/developer_manual/client_apis/OCS/ocs-share-api.html#delete-share)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `shareId` | path | `string` | yes | Numeric share ID. |
