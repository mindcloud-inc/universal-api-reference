# List Signals by Type with BuildBetter

## Endpoint

- **Method:** `POST`
- **Path:** `/graphql`
- **Base URL:** `https://api.buildbetter.app/v1`
- **Official documentation:** [List Signals by Type](https://docs.buildbetter.ai/pages/api/data-access#signals-extractions)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `typeName` | body | `string` | yes | Return only signals with this BuildBetter signal type. |
| `limit` | body | `number` | no | Maximum number of signals to return. |
