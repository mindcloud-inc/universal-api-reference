# Get Proof Comment with Ziflow

Retrieves a proof comment from Ziflow by ID.

## Endpoint

- **Method:** `GET`
- **Path:** `/proofs/:id/comments/:commentId`
- **Base URL:** `https://api.ziflow.io/v1`
- **Official documentation:** [Get Proof Comment](https://api-docs.ziflow.com/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `comment_id` | path | `string` | yes | The comment ID. |
| `id` | path | `string` | yes | The proof ID. |
