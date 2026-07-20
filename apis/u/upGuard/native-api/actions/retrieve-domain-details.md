# Retrieve Domain Details with UpGuard

Retrieves details for a domain in UpGuard.

## Endpoint

- **Method:** `GET`
- **Path:** `/domain`
- **Base URL:** `https://cyber-risk.upguard.com/api/public`
- **Official documentation:** [Retrieve Domain Details](https://cyber-risk.upguard.com/api/docs#operation/domain_details)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `hostname` | query | `string` | yes | The hostname for which to return the details, e.g. "upguard.com" |
