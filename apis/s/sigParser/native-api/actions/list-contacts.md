# List Contacts with SigParser

## Endpoint

- **Method:** `POST`
- **Path:** `/api/Contacts/List`
- **Base URL:** `https://ipaas.sigparser.com`
- **Official documentation:** [List Contacts](https://ipaas.sigparser.com/v1#post-api-contacts-list)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `page` | body | `number` | no | Page 1 is the first page of results. |
| `take` | body | `number` | no | How many contacts per page. Max 200. |
