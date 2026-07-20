# Create Debt with Raklet

## Endpoint

- **Method:** `POST`
- **Path:** `/organisations/:organisationId/debts`
- **Base URL:** `https://api.raklet.com`
- **Official documentation:** [Create Debt](https://api.raklet.com/swagger/ui/index#/AdminDebts/AdminDebts_PostDebts)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `organisationMembershipId` | body | `string` | no |
| `amount` | body | `number` | no |
| `debtType` | body | `number` | no |
