# Delete Company Notification Email Address with Recommand

Deletes a company notification email address from Recommand.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/api/v1/companies/:companyId/notification-email-addresses/:notificationEmailAddressId`
- **Base URL:** `https://app.recommand.eu`
- **Official documentation:** [Delete Company Notification Email Address](https://recommand.eu/en/reference/company-notification-email-addresses/delete-company-notification-email-address)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `companyId` | path | `string` | yes | companyId parameter. |
| `notificationEmailAddressId` | path | `string` | yes | notificationEmailAddressId parameter. |
