# Send Share Email with Next Cloud OCS

Sends a share email in Next Cloud OCS.

## Endpoint

- **Method:** `POST`
- **Path:** `/ocs/v2.php/apps/files_sharing/api/v1/shares/{{shareId}}/send-email`
- **Base URL:** `https://demo2.nextcloud.com`
- **Official documentation:** [Send Share Email](https://docs.nextcloud.com/server/latest/developer_manual/client_apis/OCS/ocs-share-api.html#send-email)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `shareId` | path | `string` | yes | Numeric share ID. |
