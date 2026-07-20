# Get Company with CallRail

Retrieves a company from CallRail.

## Endpoint

- **Method:** `GET`
- **Path:** `/v3/a/:account_id/companies/:company_id.json`
- **Base URL:** `https://api.callrail.com`
- **Official documentation:** [Get Company](https://apidocs.callrail.com/#retrieving-a-single-company)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `account_id` | path | `string` | yes | The CallRail account ID. |
| `company_id` | path | `string` | yes | The CallRail company ID. |
