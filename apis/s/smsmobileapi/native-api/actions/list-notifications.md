# List Notifications with Smsmobileapi

Retrieves notifications from Smsmobileapi.

## Endpoint

- **Method:** `GET`
- **Path:** `/notification/list/`
- **Base URL:** `https://api.smsmobileapi.com`
- **Official documentation:** [List Notifications](https://smsmobileapi.com/doc-notification/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `sidentifiant` | query | `string` | no | Filter notifications by the target mobile identifier. |
| `distribued` | query | `list` | no | Limit results to distributed or not-distributed notifications. Accepted values: `0`, `1`. |
| `date_from` | query | `date` | no | Only include notifications sent from this date forward. |
| `date_to` | query | `date` | no | Only include notifications sent up to this date. |
