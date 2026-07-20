# Send Call Using Pathways (Simple) with Bland AI

Creates a pathway-based call in Bland AI.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/calls`
- **Base URL:** `https://api.bland.ai`
- **Official documentation:** [Send Call Using Pathways (Simple)](https://docs.bland.ai/api-v1/post/calls-simple-pathway)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `phone_number` | body | `string` | yes |
| `pathway_id` | body | `string` | yes |
