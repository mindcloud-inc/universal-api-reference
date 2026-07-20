# Update Out Of Office with Next Cloud OCS

Updates out-of-office settings in Next Cloud OCS.

## Endpoint

- **Method:** `POST`
- **Path:** `/ocs/v2.php/apps/dav/api/v1/outOfOffice/{{userId}}`
- **Base URL:** `https://demo2.nextcloud.com`
- **Official documentation:** [Update Out Of Office](https://docs.nextcloud.com/server/latest/developer_manual/client_apis/OCS/ocs-out-of-office-api.html#modify-out-of-office-data)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `firstDay` | body | `string` | yes | First day in YYYY-MM-DD format. |
| `lastDay` | body | `string` | yes | Last day in YYYY-MM-DD format. |
| `message` | body | `string` | yes | Out-of-office message. |
| `status` | body | `string` | yes | Short status text shown during absence. |
| `userId` | path | `string` | yes | Nextcloud user ID. |
