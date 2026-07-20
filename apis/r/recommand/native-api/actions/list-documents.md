# List Documents with Recommand

Retrieves document records from the Recommand API.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v1/documents`
- **Base URL:** `https://app.recommand.eu`
- **Official documentation:** [List Documents](https://recommand.eu/en/reference/documents/list-documents)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `companyId` | query | `string` | no | companyId parameter. |
| `direction` | query | `string` | no | direction parameter. |
| `envelopeId` | query | `string` | no | envelopeId parameter. |
| `excludeAttachments` | query | `boolean` | no | excludeAttachments parameter. |
| `from` | query | `string` | no | from parameter. |
| `isUnread` | query | `string` | no | isUnread parameter. |
| `search` | query | `string` | no | search parameter. |
| `to` | query | `string` | no | to parameter. |
| `type` | query | `string` | no | type parameter. |
