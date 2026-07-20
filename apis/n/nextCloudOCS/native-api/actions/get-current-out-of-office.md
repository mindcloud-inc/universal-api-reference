# Get Current Out Of Office with Next Cloud OCS

Retrieves current out-of-office settings from Next Cloud OCS.

## Endpoint

- **Method:** `GET`
- **Path:** `/ocs/v2.php/apps/dav/api/v1/outOfOffice/{{userId}}/now`
- **Base URL:** `https://demo2.nextcloud.com`
- **Official documentation:** [Get Current Out Of Office](https://docs.nextcloud.com/server/latest/developer_manual/client_apis/OCS/ocs-out-of-office-api.html#fetch-ongoing-data)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `userId` | path | `string` | yes | Nextcloud user ID. |
