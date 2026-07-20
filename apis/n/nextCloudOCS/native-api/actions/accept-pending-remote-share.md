# Accept Pending Remote Share with Next Cloud OCS

Accepts a pending remote share in Next Cloud OCS.

## Endpoint

- **Method:** `POST`
- **Path:** `/ocs/v2.php/apps/files_sharing/api/v1/remote_shares/pending/{{shareId}}`
- **Base URL:** `https://demo2.nextcloud.com`
- **Official documentation:** [Accept Pending Remote Share](https://docs.nextcloud.com/server/latest/developer_manual/client_apis/OCS/ocs-share-api.html#accept-a-pending-federated-cloud-share)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `shareId` | path | `string` | yes | Pending remote share ID. |
