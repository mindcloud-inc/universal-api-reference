# List Landing Page Recipients with Smoove

Retrieves subscribers for a Smoove landing page.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/LandingPages/:id/Recipients`
- **Base URL:** `https://rest.smoove.io`
- **Official documentation:** [List Landing Page Recipients](https://rest.smoove.io)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `id` | path | `string` | yes |
| `fields` | query | `string` | no |
| `includeCustomFields` | query | `boolean` | no |
| `includeLinkedLists` | query | `boolean` | no |
