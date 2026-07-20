# Get Organization Plan Limits with Bitly

Retrieves organization plan limits from Bitly.

## Endpoint

- **Method:** `GET`
- **Path:** `/organizations/:organization_guid/plan_limits`
- **Base URL:** `https://api-ssl.bitly.com/v4`
- **Official documentation:** [Get Organization Plan Limits](https://dev.bitly.com/api-reference#getPlanLimits)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `organization_guid` | path | `string` | yes | The Bitly organization GUID. |
