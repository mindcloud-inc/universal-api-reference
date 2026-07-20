# Update Location By ID with Coast

## Endpoint

- **Method:** `PATCH`
- **Path:** `/v2/locations/:locationId`
- **Base URL:** `https://public.coastpay.com`
- **Official documentation:** [Update Location By ID](https://coastpay.com/integrations/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `locationId` | path | `string` | yes | Coast location ID of the location to update. |
| `name` | body | `string` | no | Updated name for the location. |
| `streetAddress` | body | `string` | no | Updated street address for the location. |
| `streetAddress2` | body | `string` | no | Updated second street-address line for the location. |
| `city` | body | `string` | no | Updated city for the location. |
| `state` | body | `string` | no | Updated state for the location. |
| `zip` | body | `string` | no | Updated ZIP code for the location. |
