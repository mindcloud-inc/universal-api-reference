# Download Received Fax with Notifyre SMS

Downloads a received fax from Notifyre.

## Endpoint

- **Method:** `GET`
- **Path:** `/fax/received/:faxId/download`
- **Base URL:** `https://api.notifyre.com/20220711`
- **Official documentation:** [Download Received Fax](https://docs.notifyre.com/api/fax-received-download)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `faxId` | path | `string` | yes | Received fax identifier. |
