# List Signals by Date Range with BuildBetter

## Endpoint

- **Method:** `POST`
- **Path:** `/graphql`
- **Base URL:** `https://api.buildbetter.app/v1`
- **Official documentation:** [List Signals by Date Range](https://docs.buildbetter.ai/pages/api/data-access#signals-extractions)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `dateFrom` | body | `string` | yes | Start of the display timestamp window. |
| `dateTo` | body | `string` | yes | End of the display timestamp window. |
| `limit` | body | `number` | no | Maximum number of signals to return. |
