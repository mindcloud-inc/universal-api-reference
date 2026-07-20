# List Contacts with Umbler Talk

Retrieves contacts from Umbler Talk.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/contacts/`
- **Base URL:** `https://app-utalk.umbler.com/api`
- **Official documentation:** [List Contacts](https://app-utalk.umbler.com/api/docs/index.html)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `organizationId` | query | `string` | yes | The organization ID. |
