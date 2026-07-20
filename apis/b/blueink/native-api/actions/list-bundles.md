# List Bundles with Blueink

Retrieves bundles from your Blueink account.

## Endpoint

- **Method:** `GET`
- **Path:** `/bundles/`
- **Base URL:** `https://api.blueink.com/api/v2`
- **Official documentation:** [List Bundles](https://developer.blueink.com/api/#tag/Bundles/operation/listBundles)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `search` | query | `string` | no | Search bundle slug, label, custom key, signer name, email, or phone. |
| `status` | query | `string` | no | — |
| `status__in` | query | `string` | no | Comma-separated bundle statuses to include. |
| `tag` | query | `string` | no | — |
| `tag__in` | query | `string` | no | Comma-separated tags; bundles with any listed tag match. |
| `ordering` | query | `string` | no | Sort by created, sent, or completed_at. Prefix with - for descending order. |
| `template` | query | `string` | no | Filter bundles created from a specific template ID. |
