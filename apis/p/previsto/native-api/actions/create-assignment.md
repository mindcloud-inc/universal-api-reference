# Create Assignment with Previsto

Creates a new assignment in Previsto.

## Endpoint

- **Method:** `POST`
- **Path:** `/assignments`
- **Base URL:** `https://api.previsto.io`
- **Official documentation:** [Create Assignment](https://developer.previsto.com/assignments/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `contactId` | body | `string` | yes | Previsto contact ID. |
| `accountId` | body | `string` | yes | Assigned worker account ID. |
| `address.street` | body | `string` | no | Assignment street address. |
| `address.postalCode` | body | `string` | no | Assignment postal code. |
| `address.city` | body | `string` | no | Assignment city. |
| `address.countryCode` | body | `string` | no | Assignment country code. |
| `location` | body | `string` | yes | Location as [longitude, latitude]. Required by the live API. |
