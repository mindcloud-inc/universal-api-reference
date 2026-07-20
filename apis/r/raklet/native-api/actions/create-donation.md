# Create Donation with Raklet

## Endpoint

- **Method:** `POST`
- **Path:** `/organisations/:organisationId/donations`
- **Base URL:** `https://api.raklet.com`
- **Official documentation:** [Create Donation](https://api.raklet.com/swagger/ui/index#/AdminDonations/AdminDonations_PostDonations)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `organisationMembershipId` | body | `string` | no |
| `amount` | body | `number` | no |
| `paymentMethod` | body | `number` | no |
