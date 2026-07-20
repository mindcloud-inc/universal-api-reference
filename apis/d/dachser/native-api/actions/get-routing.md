# Get Routing with Dachser

Retrieves routing details for a destination from Dachser.

## Endpoint

- **Method:** `GET`
- **Path:** `/rest/v2/routings`
- **Base URL:** `https://api-gateway.dachser.com/`
- **Official documentation:** [Get Routing](https://api-portal.dachser.com/bi.b2b.portal/api/library/routing)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `branch-id` | query | `number` | yes | DACHSER dispatch branch number. |
| `division` | query | `string` | no | DACHSER division. Use T for industrial goods or F for food. |
| `country-code` | query | `string` | yes | Consignee ISO country code. |
| `postal-code` | query | `string` | yes | Consignee postal code. |
