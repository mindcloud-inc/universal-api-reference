# Get Company Notification Email Address with Recommand

Retrieves a company notification email address from Recommand.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v1/companies/:companyId/notification-email-addresses/:notificationEmailAddressId`
- **Base URL:** `https://app.recommand.eu`
- **Official documentation:** [Get Company Notification Email Address](https://recommand.eu/en/reference/company-notification-email-addresses/get-company-notification-email-address)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `companyId` | path | `string` | yes | companyId parameter. |
| `notificationEmailAddressId` | path | `string` | yes | notificationEmailAddressId parameter. |
