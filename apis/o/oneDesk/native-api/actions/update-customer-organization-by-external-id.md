# Update Customer Organization By External ID with OneDesk

Updates a customer organization in OneDesk by external ID.

## Endpoint

- **Method:** `POST`
- **Path:** `/rest/public/customer-organizations/externalId/:externalId`
- **Base URL:** `https://app.onedesk.com`
- **Official documentation:** [Update Customer Organization By External ID](https://onedesk.com/public-api/swagger.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `externalId` | path | `string` | yes | External ID of the customer organization to update. |
| `name` | body | `string` | no | Updated name for the customer organization. |
