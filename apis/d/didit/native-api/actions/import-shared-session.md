# Import Shared Session with Didit

Imports a shared session into Didit.

## Endpoint

- **Method:** `POST`
- **Path:** `https://verification.didit.me/v3/session/import-shared/`
- **Base URL:** `https://verification.didit.me/v3`
- **Official documentation:** [Import Shared Session](https://docs.didit.me/sessions-api/share-session/import)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `share_token` | body | `string` | yes |
| `trust_review` | body | `boolean` | yes |
| `vendor_data` | body | `string` | no |
| `workflow_id` | body | `string` | yes |
