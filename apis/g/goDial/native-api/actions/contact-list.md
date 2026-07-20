# List Contacts with GoDial

Retrieves contacts from a specific GoDial contact list.

## Endpoint

- **Method:** `GET`
- **Path:** `/externals/contact/list/[:listId]`
- **Base URL:** `https://enterprise.godial.cc/meta/api`
- **Official documentation:** [List Contacts](https://godial.stoplight.io/docs/godial/b3A6MzAzMTY2MA-contact-list)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `listId` | path | `string` | yes | GoDial list ID. |
