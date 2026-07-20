# Create Property Contact with Aspire

Creates a new property contact in your Aspire account.

## Endpoint

- **Method:** `POST`
- **Path:** `PropertyContacts`
- **Base URL:** `https://{environment}.youraspire.com/`
- **Official documentation:** [Create Property Contact](https://cloud-api.youraspire.com/swagger/index.html#/PropertyContacts/PropertyContacts_Create)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `PropertyID` | body | `number` | no |
| `ContactID` | body | `number` | no |
| `PrimaryContact` | body | `boolean` | no |
| `BillingContact` | body | `boolean` | no |
| `EmailInvoiceContact` | body | `boolean` | no |
| `EmailNotificationsContact` | body | `boolean` | no |
| `SMSNotificationsContact` | body | `boolean` | no |
