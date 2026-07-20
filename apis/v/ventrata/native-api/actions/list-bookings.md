# List Bookings with Ventrata

Retrieves bookings from Ventrata.

## Endpoint

- **Method:** `GET`
- **Path:** `octo/bookings`
- **Base URL:** `https://api.ventrata.com`
- **Official documentation:** [List Bookings](https://docs.ventrata.com/octo-core/bookings#get-bookings)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `resellerReference` | query | `string` | no | Primary filter by reseller booking reference. |
| `supplierReference` | query | `string` | no | Primary filter by supplier booking reference. |
| `localDate` | query | `string` | no | Primary filter by booking local date (YYYY-MM-DD). |
| `localDateStart` | query | `string` | no | Primary filter start date; must be paired with localDateEnd. |
| `localDateEnd` | query | `string` | no | Primary filter end date; must be paired with localDateStart. |
| `availabilityId` | query | `string` | no | Primary filter by availability identifier. |
| `utcCreatedAtStart` | query | `string` | no | Primary filter start timestamp; must be paired with utcCreatedAtEnd. |
| `utcCreatedAtEnd` | query | `string` | no | Primary filter end timestamp; must be paired with utcCreatedAtStart. |
| `utcUpdatedAtStart` | query | `string` | no | Primary filter start timestamp; must be paired with utcUpdatedAtEnd. |
| `utcUpdatedAtEnd` | query | `string` | no | Primary filter end timestamp; must be paired with utcUpdatedAtStart. |
| `utcRedeemedAtStart` | query | `string` | no | Primary filter start timestamp; must be paired with utcRedeemedAtEnd. |
| `utcRedeemedAtEnd` | query | `string` | no | Primary filter end timestamp; must be paired with utcRedeemedAtStart. |
| `utcNoshowedAtStart` | query | `string` | no | Primary filter start timestamp; must be paired with utcNoshowedAtEnd. |
| `utcNoshowedAtEnd` | query | `string` | no | Primary filter end timestamp; must be paired with utcNoshowedAtStart. |
| `utcRebookedAtStart` | query | `string` | no | Primary filter start timestamp; must be paired with utcRebookedAtEnd. |
| `utcRebookedAtEnd` | query | `string` | no | Primary filter end timestamp; must be paired with utcRebookedAtStart. |
| `utcCancelledAtStart` | query | `string` | no | Primary filter start timestamp; must be paired with utcCancelledAtEnd. |
| `utcCancelledAtEnd` | query | `string` | no | Primary filter end timestamp; must be paired with utcCancelledAtStart. |
| `contactEmailAddress` | query | `string` | no | Primary filter by contact email address. |
| `contactPhoneNumber` | query | `string` | no | Primary filter by contact phone number. |
| `contactLastName` | query | `string` | no | Primary filter by contact last name. Must be at least 3 characters. |
| `status` | query | `string` | no | Optional booking status filter. |
| `tag` | query | `string` | no | Optional filter by booking tag. |
| `productId` | query | `string` | no | Optional filter by product identifier. |
| `optionId` | query | `string` | yes | Option filter. Use DEFAULT for the default option. |
| `page` | query | `number` | no | Optional page number. |
| `perPage` | query | `number` | no | Optional page size. |
