# Create Contact with DitLead

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/contact`
- **Base URL:** `https://api.ditlead.com`
- **Official documentation:** [Create Contact](https://ditlead.com/developer/api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `attributes` | body | `object` | yes | Contact attributes (for example first_name, last_name, email, company). |
| `campaignId` | body | `string` | no | Optional campaign ID to add the contact to. |
| `listId` | body | `string` | no | Optional public ID of a list to add the contact to. |
