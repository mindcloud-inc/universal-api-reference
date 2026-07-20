# Copy Other Contact To My Contacts Group with Google Contacts

Copies an other contact to My Contacts in Google Contacts.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/otherContacts/:resourceName:copyAction`
- **Base URL:** `https://people.googleapis.com`
- **Official documentation:** [Copy Other Contact To My Contacts Group](https://developers.google.com/people/api/rest/v1/otherContacts/copyOtherContactToMyContactsGroup)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `resourceName` | path | `string` | yes | — |
| `copyMask` | body | `string` | yes | Fields to copy from the other contact into My Contacts (e.g. names,emailAddresses). |
| `readMask` | body | `string` | no | Fields to include in the response person. |
| `sources[]` | body | `array<string>` | no | — |
