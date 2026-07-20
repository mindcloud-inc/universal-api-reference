# List Updated Contacts with SigParser

## Endpoint

- **Method:** `POST`
- **Path:** `/api/Contacts/List`
- **Base URL:** `https://ipaas.sigparser.com`
- **Official documentation:** [List Updated Contacts](https://ipaas.sigparser.com/v1#post-api-contacts-list)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `lastmodified_after` | body | `number` | yes | Only get contacts whose lastmodified value is greater than or equal to this value. |
| `page` | body | `number` | no | Page 1 is the first page of results. |
| `take` | body | `number` | no | How many contacts per page. Max 200. |
