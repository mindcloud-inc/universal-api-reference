# Create Customer Membership with ServiceTitan

Creates a customer membership sale in ServiceTitan.

## Endpoint

- **Method:** `POST`
- **Path:** `memberships/v2/tenant/{tenant}/memberships/sale`
- **Base URL:** `https://{baseUrl}/`
- **Official documentation:** [Create Customer Membership](https://developer.servicetitan.io/api-details/#api=tenant-memberships-v2&operation=CustomerMemberships_Create)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `customerId` | body | `number` | yes | ID of the customer you are creating the Membership Sale Invoice for |
| `businessUnitId` | body | `number` | yes | Business unit ID |
| `saleTaskId` | body | `number` | yes | ID of the sale task that is creating the membership |
| `durationBillingId` | body | `number` | yes | ID of the duration/billing option to be used |
| `locationId` | body | `number` | no | — |
| `recurringServiceAction` | body | `string` | yes | Required if RecurringLocationId is set. Determines how many of the customer's locations that recurring services should be added to: all, single, or none (which deletes existing recurring services). |
| `recurringLocationId` | body | `number` | no | — |
