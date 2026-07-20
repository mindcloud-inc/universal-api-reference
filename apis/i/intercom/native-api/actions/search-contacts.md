# Search Contacts with Intercom

## Endpoint

- **Method:** `POST`
- **Path:** `/contacts/search`
- **Base URL:** `https://api.intercom.io`
- **Official documentation:** [Search Contacts](https://developers.intercom.com/docs/references/rest-api/api.intercom.io/contacts/searchcontacts)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `query` | body | `object` | no | — |
| `query.field` | body | `string` | yes | Field to search by |
| `query.operator` | body | `string` | yes | Search operator |
| `query.value` | body | `string` | yes | Value to match |
