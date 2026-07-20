# List Do Not Contact List with SmartReach

Retrieves do not contact entries from SmartReach.

## Endpoint

- **Method:** `GET`
- **Path:** `/do_not_contact`
- **Base URL:** `https://api.smartreach.io/api/v3`
- **Official documentation:** [List Do Not Contact List](https://help.smartreach.io/reference/getdnc)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `older_than` | query | `number` | no | timestamp in unix epoch milliseconds |
| `newer_than` | query | `number` | no | timestamp in unix epoch milliseconds |
