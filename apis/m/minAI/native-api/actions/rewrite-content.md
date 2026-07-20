# Rewrite content with 1minAI

Creates rewritten text content in 1minAI.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/features`
- **Base URL:** `https://api.1min.ai`
- **Official documentation:** [Rewrite content](https://docs.1min.ai/docs/api/ai-for-writing/rewriter/rewriter-tag)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `prompt` | body | `string` | yes |
| `tone` | body | `string` | no |
| `numberOfWord` | body | `number` | no |
