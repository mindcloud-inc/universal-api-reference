# List Signals by Sentiment with BuildBetter

## Endpoint

- **Method:** `POST`
- **Path:** `/graphql`
- **Base URL:** `https://api.buildbetter.app/v1`
- **Official documentation:** [List Signals by Sentiment](https://docs.buildbetter.ai/pages/api/data-access#signals-extractions)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `sentiment` | body | `number` | yes | Return only signals matching this sentiment score. |
| `limit` | body | `number` | no | Maximum number of signals to return. |
