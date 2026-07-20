# Get Organization with Bitly

Retrieves an organization from your Bitly account.

## Endpoint

- **Method:** `GET`
- **Path:** `/organizations/:organization_guid`
- **Base URL:** `https://api-ssl.bitly.com/v4`
- **Official documentation:** [Get Organization](https://dev.bitly.com/api-reference#getOrganization)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `organization_guid` | path | `string` | yes | The Bitly organization GUID. |
