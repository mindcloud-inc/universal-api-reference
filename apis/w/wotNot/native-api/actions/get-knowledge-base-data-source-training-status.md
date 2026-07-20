# Get Knowledge Base Data Source Training Status with WotNot

Retrieves knowledge base source training status from WotNot.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v1/ai/status/sources`
- **Base URL:** `https://api.wotnot.io`
- **Official documentation:** [Get Knowledge Base Data Source Training Status](https://help.wotnot.io/build/integrations/public-apis)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `source_ids` | query | `string` | yes | Comma-separated knowledge base source IDs |
