# Create Domain with Markup AI

Creates a new terminology domain in Markup AI.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/terminology/domains`
- **Base URL:** `https://api.markup.ai`
- **Official documentation:** [Create Domain](https://docs.markup.ai/api-reference/terminology/create-domain)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | Name of the terminology domain. |
| `description` | body | `string` | no | Optional description for the terminology domain. |
