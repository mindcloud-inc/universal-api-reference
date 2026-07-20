# Get Share with Next Cloud OCS

Retrieves share details from Next Cloud OCS.

## Endpoint

- **Method:** `GET`
- **Path:** `/ocs/v2.php/apps/files_sharing/api/v1/shares/{{shareId}}`
- **Base URL:** `https://demo2.nextcloud.com`
- **Official documentation:** [Get Share](https://docs.nextcloud.com/server/latest/developer_manual/client_apis/OCS/ocs-share-api.html#get-information-about-a-known-share)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `shareId` | path | `string` | yes | Numeric share ID. |
