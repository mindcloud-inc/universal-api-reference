# Get User Metadata with Next Cloud OCS

Retrieves user metadata from Next Cloud OCS.

## Endpoint

- **Method:** `GET`
- **Path:** `/ocs/v1.php/cloud/users/{{userId}}`
- **Base URL:** `https://demo2.nextcloud.com`
- **Official documentation:** [Get User Metadata](https://docs.nextcloud.com/server/latest/developer_manual/client_apis/OCS/ocs-api-overview.html#user-metadata)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `userId` | path | `string` | yes | Nextcloud user ID. |
