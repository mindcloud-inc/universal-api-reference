# Update Organization with Paycove

Updates an organization in Paycove.

## Endpoint

- **Method:** `PATCH`
- **Path:** `organizations/:id`
- **Base URL:** `https://paycove.io/api/v1`
- **Official documentation:** [Update Organization](https://docs.paycove.io/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Paycove CRMOrganization ID. |
| `name` | query | `string` | no | Organization name. |
| `email` | query | `string` | no | Organization email. |
| `phone` | query | `string` | no | Organization phone. |
| `line1` | query | `string` | no | Street address. |
| `city` | query | `string` | no | City. |
| `state` | query | `string` | no | State or region. |
| `country` | query | `string` | no | Country. |
| `postal_code` | query | `string` | no | Postal code. |
| `owner_id` | query | `string` | no | Organization owner ID. |
| `twitter` | query | `string` | no | Organization Twitter. |
| `facebook` | query | `string` | no | Organization Facebook. |
| `linkedin` | query | `string` | no | Organization LinkedIn. |
| `industry` | query | `string` | no | Organization industry. |
| `website` | query | `string` | no | Organization website. |
