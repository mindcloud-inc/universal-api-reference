# Update Contact with Cliengo

## Endpoint

- **Method:** `PATCH`
- **Path:** `/contacts/:contactId`
- **Base URL:** `https://api.cliengo.com/1.0`
- **Official documentation:** [Update Contact](https://developers.cliengo.com/reference/contactscontactid)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `contactId` | path | `string` | yes | Identifier of the Cliengo contact. |
| `name` | body | `string` | no | Contact name. |
| `email` | body | `string` | no | Contact email. |
| `phone` | body | `string` | no | Contact phone number. |
| `status` | body | `string` | no | Contact status. Possible values include NEW, ACTIVE, LONG_TERM, and CLIENT. |
| `subStatus` | body | `string` | no | Contact sub-status. |
| `rating` | body | `number` | no | Contact rating from 0 to 5. |
| `assignedTo` | body | `string` | no | User ID to assign the contact to, or UNASSIGNED. |
| `dueDate` | body | `date` | no | Scheduled due date for the contact. |
| `contactMethod` | body | `string` | no | Entry method such as WHATSAPP, FB_LEADADS, FORM, CHATBOT, API, or ZAPIER. |
| `note` | body | `string` | no | Simple note stored on the contact log. |
| `scheduleStatusTo` | body | `string` | no | Future status to apply on the scheduled date. |
| `scheduleDate` | body | `date` | no | Date when the scheduled status should replace the current status. |
| `sellPrice` | body | `number` | no | Contact sell price. |
| `sellSuscription` | body | `string` | no | Sell subscription type such as ONE_TIME, MONTHLY_SUSCRIPTION, YEARLY_SUSCRIPTION, or OTHER_SELL_TYPE. |
| `cancelReason` | body | `string` | no | Cancellation reason code from 1 to 5. |
| `extraParams` | body | `object` | no | Additional custom parameters object. |
