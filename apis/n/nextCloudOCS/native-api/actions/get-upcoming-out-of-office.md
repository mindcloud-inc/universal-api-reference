# Get Upcoming Out Of Office with Next Cloud OCS

Retrieves upcoming out-of-office settings from Next Cloud OCS.

## Endpoint

- **Method:** `GET`
- **Path:** `/ocs/v2.php/apps/dav/api/v1/outOfOffice/{{userId}}`
- **Base URL:** `https://demo2.nextcloud.com`
- **Official documentation:** [Get Upcoming Out Of Office](https://docs.nextcloud.com/server/latest/developer_manual/client_apis/OCS/ocs-out-of-office-api.html#fetch-upcoming-or-ongoing-data)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `userId` | path | `string` | yes | Nextcloud user ID. |
