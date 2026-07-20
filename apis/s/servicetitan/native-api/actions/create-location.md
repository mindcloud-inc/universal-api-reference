# Create Location with ServiceTitan

## Endpoint

- **Method:** `POST`
- **Path:** `crm/v2/tenant/{tenant}/locations`
- **Base URL:** `https://{baseUrl}/`

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `address.street` | body | `string` | no |
| `contacts[].type` | body | `list<string>` | no |
| `externalData.externalData[]` | body | `array` | no |
| `name` | body | `string` | no |
| `address` | body | `object` | no |
| `address.city` | body | `string` | no |
| `contacts[].value` | body | `string` | no |
| `externalData.applicationGuid` | body | `string` | no |
| `address.state` | body | `string` | no |
| `customerId` | body | `number` | no |
| `address.zip` | body | `string` | no |
| `externalData` | body | `object` | no |
| `address.country` | body | `string` | no |
| `contacts[]` | body | `array` | no |
| `address.unit` | body | `string` | no |
