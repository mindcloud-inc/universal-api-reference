# Create Contact with Karma CRM

Creates a new contact in Karma CRM.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v3/contacts.json`
- **Base URL:** `https://app.karmacrm.com`
- **Official documentation:** [Create Contact](https://docs.karmacrm.com/#create-a-contact)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `contact` | body | `object` | yes | Contact payload object exactly as documented by Karma CRM. Pass the nested contact fields inside this object. |
