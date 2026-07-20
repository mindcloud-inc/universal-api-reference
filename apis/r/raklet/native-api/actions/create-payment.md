# Create Payment with Raklet

## Endpoint

- **Method:** `POST`
- **Path:** `/organisations/:organisationId/payments`
- **Base URL:** `https://api.raklet.com`
- **Official documentation:** [Create Payment](https://api.raklet.com/swagger/ui/index#/AdminPayments/AdminPayments_PostPayments)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `organisationMembershipId` | body | `string` | no |
| `amount` | body | `number` | yes |
| `currency` | body | `number` | yes |
| `paymentMethod` | body | `number` | yes |
