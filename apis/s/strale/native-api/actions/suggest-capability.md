# Suggest Capability with Strale

Suggests capabilities or solutions in Strale for a query.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/suggest`
- **Base URL:** `https://api.strale.io`
- **Official documentation:** [Suggest Capability](https://strale.dev/docs#api-suggest)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `limit` | body | `number` | no | Maximum number of suggestions to return. |
| `query` | body | `string` | yes | Natural language query for capability or solution suggestions. |
