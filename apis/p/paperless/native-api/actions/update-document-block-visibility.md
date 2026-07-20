# Update Document Block Visibility with Paperless

## Endpoint

- **Method:** `PATCH`
- **Path:** `/documents/:id`
- **Base URL:** `https://app.paperless.io/api/v1`
- **Official documentation:** [Update Document Block Visibility](https://developers.paperless.io/docs/api/2ba41f7dfe8a3-visibility-of-blocks)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | The Paperless document ID. |
| `blocks` | body | `object` | yes | Block visibility overrides keyed by block slug. |
