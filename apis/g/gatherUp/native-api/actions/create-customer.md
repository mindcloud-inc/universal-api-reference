# Create Customer with GatherUp

Creates a new customer in GatherUp.

## Endpoint

- **Method:** `POST`
- **Path:** `/customer/create`
- **Base URL:** `https://app.gatherup.com/api`
- **Official documentation:** [Create Customer](https://app.gatherup.com/api/doc/customer/create)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `businessId` | body | `number` | yes | Business id. |
| `customerCustomId` | body | `string` | no | Customer custom id. |
| `customerEmail` | body | `string` | yes | Customer email address. This field is required for basic plan accounts. For higher plans there is email or phone number required. |
| `customerFirstName` | body | `string` | yes | Customer first name. |
| `customerJobId` | body | `string` | no | Customer job id. |
| `customerLastName` | body | `string` | yes | Customer last name. |
| `customerPhone` | body | `string` | no | Customer mobile phone. |
| `customerTags` | body | `string` | no | Customer tags separated by comma (max length of one tag = 50 chars). |
| `delayFeedbackRequest` | body | `number` | no | 0 will send feedback immediately -> if "sendFeedbackRequest" parameter is set to 1. If you set delayFeedbackRequest to anything over 0, it will delay that many hours before the feedback request is sent. Important the Communication Preference in the customer dashboard must be set to "Manual Mode". The "delayFeedbackRequest" parameter will be ignored if set to"Automatic Mode". |
| `customerPreference` | body | `string` | no | Customer communication preference. |
| `preferenceChecking` | body | `number` | no | If the parameter is set to 0 then Customer Preference is set according to the data provided (`customerEmail` or `customerPhone`) regardless of the `customerPreference` field value. |
| `sendFeedbackRequest` | body | `number` | no | Send feedback request email to the customer right away. |
