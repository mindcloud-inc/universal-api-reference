# List Contacts with PhoneBurner

Retrieves a list of contacts from PhoneBurner.

## Endpoint

- **Method:** `GET`
- **Path:** `rest/1/contacts`
- **Base URL:** `https://www.phoneburner.com/`
- **Official documentation:** [List Contacts](https://www.phoneburner.com/developer/route_list#contacts)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `email_address` | query | `string` | no | Optional email address filter. |
| `page` | query | `string` | no | Page number to fetch. |
| `page_size` | query | `string` | no | Number of contacts to fetch per page. |
