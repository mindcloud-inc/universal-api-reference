# Update Form Mailchimp Integration with Kite Suite

## Endpoint

- **Method:** `PATCH`
- **Path:** `/api/v1/form/integration/mailchimp/:id`
- **Base URL:** `https://api.kitesuite.com`
- **Official documentation:** [Update Form Mailchimp Integration](https://api.kitesuite.com/swagger/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `body` | body | `object` | yes | Request body |
| `id` | path | `string` | yes | ID of the Mailchimp integration to update. |
| `listId` | body | `string` | yes | Updated ID of the Mailchimp list. |
| `tagType` | body | `string` | yes | Updated type of Mailchimp tags. |
| `staticTags[]` | body | `array` | yes | Updated array of static Mailchimp tags. |
| `dynamicTag` | body | `string` | yes | Updated ID of the form field for dynamic Mailchimp tag. |
| `sendContact` | body | `string` | yes | Updated how to send contact to Mailchimp. |
| `consentMessage` | body | `string` | yes | Updated consent message for Mailchimp. |
| `isUpdateExistingContact` | body | `boolean` | yes | Updated flag to update existing contact in Mailchimp. |
| `isAddExistingContact` | body | `boolean` | yes | Updated flag to add existing contact in Mailchimp. |
| `isSendOptIn` | body | `boolean` | yes | Updated flag to send opt-in email to contact. |
| `fields[]` | body | `array` | yes | Updated array of Mailchimp fields and corresponding form fields. |
