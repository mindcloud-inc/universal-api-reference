# List Publication Email Blasts with Beehiiv

Retrieves email blasts for a publication from Beehiiv.

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/publications/:publicationId/email_blasts`
- **Base URL:** `https://api.beehiiv.com`
- **Official documentation:** [List Publication Email Blasts](https://files.buildwithfern.com/https%3A//beehiiv.docs.buildwithfern.com/d0f4c30b8707ec784c673704353550d3fb9e00a41983b8f2e3d852f96d93abdb/assets/beehiiv-API-Specification.yaml)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `publicationId` | path | `string` | yes | The prefixed ID of the publication object. |
| `expand[]` | query | `array<string>` | no | Optional list of expandable objects. |
| `status` | query | `string` | no | Optionally filter by email blast status. |
| `limit` | query | `number` | no | A limit on the number of objects to be returned. |
| `page` | query | `number` | no | Page number for pagination. |
| `order_by` | query | `string` | no | The field that the results are sorted by. |
| `direction` | query | `string` | no | The direction that the results are sorted in. |
