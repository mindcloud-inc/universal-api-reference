# Merge Conversations with Missive

Merges conversations in your Missive workspace.

## Endpoint

- **Method:** `POST`
- **Path:** `/conversations/:id/merge`
- **Base URL:** `https://public.missiveapp.com/v1`
- **Official documentation:** [Merge Conversations](https://missiveapp.com/docs/developers/rest-api/endpoints#merge-conversations)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Source conversation ID to merge. |
| `target` | body | `string` | yes | Target conversation ID. |
| `subject` | body | `string` | no | Optional subject to set on the merged conversation. |
