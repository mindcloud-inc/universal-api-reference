# Create Client with OneSuite

Creates a client in OneSuite.

## Endpoint

- **Method:** `POST`
- **Path:** `/v2/clients`
- **Base URL:** `https://api.onesuite.io`
- **Official documentation:** [Create Client](https://rest-api.onesuite.io/#create-client-with-all-fields)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `type` | body | `list` | yes | Type of client: company or individual Accepted values: `0`, `1`. |
| `name` | body | `string` | yes | Client name |
