# List Orders with Ventrata

Retrieves orders from Ventrata.

## Endpoint

- **Method:** `GET`
- **Path:** `octo/orders`
- **Base URL:** `https://api.ventrata.com`
- **Official documentation:** [List Orders](https://docs.ventrata.com/capabilities/cart#get-orders)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `supplierReference` | query | `string` | no | Filter by exact supplier order reference. |
| `utcCreatedAtStart` | query | `string` | no | Filter start timestamp; must be paired with utcCreatedAtEnd. |
| `utcCreatedAtEnd` | query | `string` | no | Filter end timestamp; must be paired with utcCreatedAtStart. |
| `utcUpdatedAtStart` | query | `string` | no | Filter start timestamp; must be paired with utcUpdatedAtEnd. |
| `utcUpdatedAtEnd` | query | `string` | no | Filter end timestamp; must be paired with utcUpdatedAtStart. |
| `contactEmailAddress` | query | `string` | no | Filter by contact email address. |
| `contactPhoneNumber` | query | `string` | no | Filter by contact phone number. |
| `contactLastName` | query | `string` | no | Filter by contact last name. |
