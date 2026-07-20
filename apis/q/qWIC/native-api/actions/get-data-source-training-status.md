# Get Data Source Training Status with QWIC

Retrieves training status for a QWIC data source.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v1/ai/status/sources`
- **Base URL:** `https://app.qwic.ai`
- **Official documentation:** [Get Data Source Training Status](https://qwic-1.gitbook.io/help/building-agents/integrations/public-apis#get-training-status-of-a-data-source)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `source_ids` | query | `list<number>` | yes | Comma-separated list of data source IDs. Send multiple values as a string separated by `,`. |
