# Delete Remote Share with Next Cloud OCS

Deletes a remote share from Next Cloud OCS.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/ocs/v2.php/apps/files_sharing/api/v1/remote_shares/{{shareId}}`
- **Base URL:** `https://demo2.nextcloud.com`
- **Official documentation:** [Delete Remote Share](https://docs.nextcloud.com/server/latest/developer_manual/client_apis/OCS/ocs-share-api.html#delete-an-accepted-federated-cloud-share)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `shareId` | path | `string` | yes | Remote share ID. |
