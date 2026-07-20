# Search using Saved Search with NetSuite - Advanced

Search using a previously saved search using NetSuite's Query Language

## Endpoint

- **Method:** `POST`
- **Path:** `https://{accountId}.restlets.api.netsuite.com/app/site/hosting/restlet.nl`
- **Base URL:** `https://{accountId}.suitetalk.api.netsuite.com`
- **API:** REST
- **Official documentation:** [Search using Saved Search](https://docs.oracle.com/en/cloud/saas/netsuite/ns-online-help/section_156257770590.html)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [filtering](../README.md#filtering).

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json; charset=utf-8` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `savedSearchId` | body | `list` | no | — |
| `savedSearchLink` | body | `object` | no | This is a display only component. |
| `savedSearchType` | body | `string` | no | Some saved searches (like Inventory Balance or System Notes) aren’t tied to a record type, so NetSuite can’t determine their type automatically. Providing the saved search type ensures the search can be loaded and executed correctly. |
| `includeIds` | body | `boolean` | no | Return the ID value of lookups in addition to their text labels. Format: `toggle`. |
