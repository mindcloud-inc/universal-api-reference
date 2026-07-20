# Search Contacts with FuseDesk

Finds contacts in FuseDesk by matching search text.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v2/contacts`
- **Base URL:** `https://{appName}.fusedesk.com`
- **Official documentation:** [Search Contacts](https://documenter.getpostman.com/view/11014835/SztBc8ix#77197b55-cc58-4087-b0da-c1f449292d8f)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `search` | query | `string` | yes | Search text for matching contacts. |
