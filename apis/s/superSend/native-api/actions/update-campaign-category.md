# Update Campaign Category with SuperSend

Updates an existing campaign category in SuperSend.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/campaign-categories`
- **Base URL:** `https://api.supersend.io/v2`
- **Official documentation:** [Update Campaign Category](https://docs.supersend.io/docs/campaign-category)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `TeamId` | body | `string` | yes | — |
| `categoryId` | body | `string` | yes | Category ID to update |
| `name` | body | `string` | yes | — |
