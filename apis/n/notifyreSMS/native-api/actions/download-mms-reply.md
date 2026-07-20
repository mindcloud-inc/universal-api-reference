# Download MMS Reply with Notifyre SMS

Downloads an MMS reply attachment from Notifyre.

## Endpoint

- **Method:** `GET`
- **Path:** `/mms/received/:replyId/download`
- **Base URL:** `https://api.notifyre.com/20220711`
- **Official documentation:** [Download MMS Reply](https://docs.notifyre.com/api/mms-received-download)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `replyId` | path | `string` | yes | Reply identifier. |
