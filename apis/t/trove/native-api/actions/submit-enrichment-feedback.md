# Submit Enrichment Feedback with Trove

Submits transaction enrichment feedback to Trove.

## Endpoint

- **Method:** `POST`
- **Path:** `/transactions/feedback`
- **Base URL:** `https://trove.headline.com/api/v1`
- **Official documentation:** [Submit Enrichment Feedback](https://trove.headline.com/docs)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `description` | body | `string` | yes | The original transaction description previously sent to Enrich Transaction. |
| `domain` | body | `string` | yes | The correct domain to associate with the transaction description. |
| `comment` | body | `string` | no | Optional feedback about the enrichment response. |
