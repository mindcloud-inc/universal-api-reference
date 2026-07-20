# Update Contact with DitLead

## Endpoint

- **Method:** `PUT`
- **Path:** `/v1/contact/{contactId}`
- **Base URL:** `https://api.ditlead.com`
- **Official documentation:** [Update Contact](https://ditlead.com/developer/api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `attributes` | body | `object` | yes | Contact attributes to update (for example first_name, company, phone). |
| `contactId` | path | `string` | yes | Public ID of the contact. |
