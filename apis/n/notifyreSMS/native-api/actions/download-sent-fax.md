# Download Sent Fax with Notifyre SMS

Downloads a sent fax from Notifyre.

## Endpoint

- **Method:** `GET`
- **Path:** `/fax/send/recipients/:recipientId/download`
- **Base URL:** `https://api.notifyre.com/20220711`
- **Official documentation:** [Download Sent Fax](https://docs.notifyre.com/api/fax-sent-download)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `fileType` | query | `string` | no | Downloaded file type. |
| `recipientId` | path | `string` | yes | Recipient identifier for the sent fax. |
