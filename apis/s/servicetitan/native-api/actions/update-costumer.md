# Update Costumer with ServiceTitan

Updates an existing customer in ServiceTitan.

## Endpoint

- **Method:** `PATCH`
- **Path:** `crm/v2/tenant/{tenant}/customers/:customerId`
- **Base URL:** `https://{baseUrl}/`

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `memo` | body | `string` | no | — |
| `address.street` | body | `string` | no | — |
| `contacts[].value` | body | `string` | no | — |
| `customFields[].typeId` | body | `number` | no | — |
| `externalData.externalData[].value` | body | `string` | no | — |
| `locations[].address.street` | body | `string` | no | — |
| `locations[].contacts[].memo` | body | `string` | no | — |
| `locations[].externalData.externalData[].value` | body | `string` | no | — |
| `locations[].name` | body | `string` | no | — |
| `name` | body | `string` | no | — |
| `address.unit` | body | `string` | no | — |
| `contacts[].type` | body | `list<string>` | no | — |
| `customFields[].value` | body | `string` | no | — |
| `externalData.applicationGuid` | body | `string` | no | — |
| `externalData.externalData[].key` | body | `string` | no | — |
| `locations[].address` | body | `object` | no | — |
| `locations[].address.unit` | body | `string` | no | — |
| `locations[].contacts[].value` | body | `string` | no | — |
| `locations[].externalData.applicationGuid` | body | `string` | no | — |
| `locations[].externalData.externalData[].key` | body | `string` | no | — |
| `address.city` | body | `string` | no | — |
| `contacts[].type` | body | `list<string>` | no | — |
| `customFields[].name` | body | `string` | no | Name/label of the custom field |
| `doNotMail` | body | `boolean` | no | Format: `toggle`. |
| `externalData.externalData[]` | body | `array` | no | — |
| `locations[].address.city` | body | `string` | no | — |
| `locations[].contacts[]` | body | `array<object>` | no | — |
| `locations[].contacts[].type` | body | `string<string>` | no | — |
| `locations[].externalData.externalData[]` | body | `array` | no | — |
| `address.state` | body | `string` | no | — |
| `doNotService` | body | `boolean` | no | Format: `toggle`. |
| `locations[].address.zip` | body | `string` | no | — |
| `locations[].tagTypeIds[]` | body | `array<number>` | no | — |
| `address.zip` | body | `string` | no | — |
| `locations[]` | body | `array<object>` | no | Locations for the customer |
| `locations[].address.state` | body | `string` | no | — |
| `locations[].externalData` | body | `object` | no | — |
| `address` | body | `object<object>` | no | Bill-To address of the customer record |
| `address.country` | body | `string` | no | — |
| `externalData` | body | `object` | no | — |
| `locations[].address.country` | body | `string` | no | — |
| `address.longitude` | body | `number` | no | — |
| `contacts[]` | body | `array<object>` | no | — |
| `locations[].latitude` | body | `number` | no | — |
| `address.latitude` | body | `number` | no | — |
| `customFields[]` | body | `array<object>` | no | — |
| `locations[].longitude` | body | `number` | no | — |
| `tagTypeIds[]` | body | `array<number>` | no | — |
| `type` | body | `string` | no | Residential or commercial |
| `customerId` | path | `string` | yes | — |
| `customFields` | body | `string` | no | — |
