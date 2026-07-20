# List Domain Contacts with Crexendo

Retrieves contacts for a domain in Crexendo.

## Endpoint

- **Method:** `GET`
- **Path:** `/domains/:domain/contacts`
- **Base URL:** `https://ns-api.com/ns-api/v2`
- **Official documentation:** [List Domain Contacts](https://docs.ns-api.com/reference/getdomaincontacts)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `domain` | path | `string` | yes | Domain identifier, for example apps.mindcloud.co. |
