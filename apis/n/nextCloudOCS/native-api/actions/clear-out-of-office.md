# Clear Out Of Office with Next Cloud OCS

Clears out-of-office settings in Next Cloud OCS.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/ocs/v2.php/apps/dav/api/v1/outOfOffice/{{userId}}`
- **Base URL:** `https://demo2.nextcloud.com`
- **Official documentation:** [Clear Out Of Office](https://docs.nextcloud.com/server/latest/developer_manual/client_apis/OCS/ocs-out-of-office-api.html#clear-data-and-disable-out-of-office)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `userId` | path | `string` | yes | Nextcloud user ID. |
