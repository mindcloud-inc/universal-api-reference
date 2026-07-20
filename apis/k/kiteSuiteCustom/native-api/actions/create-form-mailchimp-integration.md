# Create Form Mailchimp Integration with Kite Suite

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/form/integration/mailchimp`
- **Base URL:** `https://api.kitesuite.com`
- **Official documentation:** [Create Form Mailchimp Integration](https://api.kitesuite.com/swagger/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `body` | body | `object` | yes | Request body |
| `form` | body | `string` | yes | ID of the form. |
| `listId` | body | `string` | yes | ID of the Mailchimp list. |
| `tagType` | body | `string` | yes | Type of Mailchimp tags. |
| `staticTags[]` | body | `array` | yes | Array of static Mailchimp tags. |
| `dynamicTag` | body | `string` | yes | ID of the form field for dynamic Mailchimp tag. |
| `sendContact` | body | `string` | yes | How to send contact to Mailchimp. |
| `consentMessage` | body | `string` | yes | Consent message for Mailchimp. |
| `isUpdateExistingContact` | body | `boolean` | yes | Flag to update existing contact in Mailchimp. |
| `isAddExistingContact` | body | `boolean` | yes | Flag to add existing contact in Mailchimp. |
| `isSendOptIn` | body | `boolean` | yes | Flag to send opt-in email to contact. |
| `fields[]` | body | `array` | yes | Array of Mailchimp fields and corresponding form fields. |
