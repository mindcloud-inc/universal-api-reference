# Update Customer Membership with ServiceTitan

Updates an existing customer membership in ServiceTitan.

## Endpoint

- **Method:** `PATCH`
- **Path:** `memberships/v2/tenant/{tenant}/memberships/:membershipId`
- **Base URL:** `https://{baseUrl}/`
- **Official documentation:** [Update Customer Membership](https://developer.servicetitan.io/api-details/#api=tenant-memberships-v2&operation=CustomerMemberships_Update)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `membershipId` | path | `number` | no | — |
| `businessUnitId` | body | `number` | no | Business unit ID |
| `nextScheduledBillDate` | body | `string` | no | Next date that this membership will be billed on |
| `status` | body | `list` | no | — |
| `memo` | body | `string` | no | — |
| `from` | body | `date` | no | — |
| `to` | body | `date` | no | The end date of this membership (null if ongoing) |
| `billingTemplateId` | body | `number` | no | The ID of the invoice template used to bill this membership. Can either be a "settings template" (when invoice template is shared – in this case new invoice template will be created), or be a new invoice template created specifically for this customer membership. |
| `soldByID` | body | `number` | no | ID of the user that was credited for the sale of this membership |
| `locationId` | body | `number` | no | — |
| `recurringServiceAction` | body | `string` | no | Required if RecurringLocationId is set. Determines how many of the customer's locations that recurring services should be added to: all, single, or none (which deletes existing recurring services). |
| `recurringLocationId` | body | `number` | no | — |
| `cancellationBalanceInvoiceId` | body | `number` | no | — |
| `cancellationInvoiceId` | body | `number` | no | — |
| `initialDeferredRevenue` | body | `number` | no | — |
| `paymentMethodId` | body | `number` | no | — |
| `paymentTypeId` | body | `number` | no | — |
| `renewalMembershipTaskId` | body | `number` | no | — |
