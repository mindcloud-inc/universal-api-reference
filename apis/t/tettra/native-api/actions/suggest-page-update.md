# Suggest Page Update with Tettra

Creates a page update suggestion in Tettra.

## Endpoint

- **Method:** `POST`
- **Path:** `/teams/85329/suggestions`
- **Base URL:** `https://app.tettra.co/api`
- **Official documentation:** [Suggest Page Update](https://support.tettra.com/pages-2/api-endpoint-suggest-page-update)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `assignable_id` | body | `number` | no | User ID to assign the suggestion to. |
| `description` | body | `string` | no | Suggested change details. |
| `page_id` | body | `number` | yes | Page ID to suggest updates for. |
