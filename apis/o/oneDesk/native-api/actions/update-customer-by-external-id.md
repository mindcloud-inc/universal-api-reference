# Update Customer By External ID with OneDesk

Updates a customer in OneDesk by external ID.

## Endpoint

- **Method:** `POST`
- **Path:** `/rest/public/customers/externalId/:externalId`
- **Base URL:** `https://app.onedesk.com`
- **Official documentation:** [Update Customer By External ID](https://onedesk.com/public-api/swagger.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `externalId` | path | `string` | yes | External ID of the customer to update. |
| `lastName` | body | `string` | no | Updated last name for the customer. |
