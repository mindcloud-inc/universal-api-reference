# Get Account with CallRail

Retrieves an account from CallRail.

## Endpoint

- **Method:** `GET`
- **Path:** `/v3/a/:account_id.json`
- **Base URL:** `https://api.callrail.com`
- **Official documentation:** [Get Account](https://apidocs.callrail.com/#retrieving-a-single-account)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `account_id` | path | `string` | yes | The CallRail account ID. |
| `fields` | query | `string` | no | Comma-separated additional account fields to include in the response. |
