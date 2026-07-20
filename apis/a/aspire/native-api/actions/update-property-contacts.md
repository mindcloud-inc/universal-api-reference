# Update Property Contacts with Aspire

## Endpoint

- **Method:** `PUT`
- **Path:** `PropertyContacts`
- **Base URL:** `https://{environment}.youraspire.com/`
- **Official documentation:** [Update Property Contacts](https://guide.youraspire.com/apidocs/propertycontacts-7)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `PropertyID` | body | `list<number>` | yes | — |
| `ContactID` | body | `list<number>` | yes | — |
| `billingcontact` | body | `boolean` | no | Format: `toggle`. |
| `emailinvoicecontact` | body | `boolean` | no | Format: `toggle`. |
| `primarycontact` | body | `boolean` | no | Format: `toggle`. |
| `emailnotificationscontact` | body | `boolean` | no | Format: `toggle`. |
| `smsnotificationscontact` | body | `boolean` | no | Format: `toggle`. |
| `viewinaspiremobile` | body | `boolean` | no | Format: `toggle`. |
