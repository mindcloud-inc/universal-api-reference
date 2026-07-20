# Check Transfer Status with Poof

Retrieves ACH transfer status from Poof.

## Endpoint

- **Method:** `POST`
- **Path:** `https://www.poof.io/api/v2/transfer_status`
- **Base URL:** `https://www.poof.io/api/v2`
- **Official documentation:** [Check Transfer Status](https://docs.poof.io/reference/ach-transfer-status)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `transaction` | body | `string` | no | Transfer transaction identifier. |
