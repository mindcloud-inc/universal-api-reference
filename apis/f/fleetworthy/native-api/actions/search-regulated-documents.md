# Search Regulated Documents with Fleetworthy

## Endpoint

- **Method:** `POST`
- **Path:** `/people-bulk/regulated-documents/search`
- **Base URL:** `https://apis.fleetworthy.com/compliance-api/v1`
- **Official documentation:** [Search Regulated Documents](https://developer.fleetworthy.com/api-details#api=prod-compliance-v1&operation=post-people-bulk-regulated-documents-search)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `advancedFilter` | body | `object` | no | Optional regulated-document filter object containing document type, status, person, date, activity, archive, Canadian, or category filters. |
| `searchText` | body | `string` | no | Text used to search regulated documents. |
| `clientId` | body | `string` | no | The Fleetworthy client UUID. |
