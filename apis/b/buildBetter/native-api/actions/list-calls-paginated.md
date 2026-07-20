# List Calls Paginated with BuildBetter

## Endpoint

- **Method:** `POST`
- **Path:** `/graphql`
- **Base URL:** `https://api.buildbetter.app/v1`
- **Official documentation:** [List Calls Paginated](https://docs.buildbetter.ai/pages/api/graphql-examples#offset-pagination)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `limit` | body | `number` | no | Maximum number of calls to return. |
| `offset` | body | `number` | no | Number of calls to skip before returning results. |
