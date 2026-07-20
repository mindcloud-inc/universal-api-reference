# Get Annotation By ID with Grafana

Retrieves an annotation from Grafana by ID.

## Endpoint

- **Method:** `GET`
- **Path:** `/annotations/:annotation_id`
- **Base URL:** `https://apps78aa.grafana.net/api`
- **Official documentation:** [Get Annotation By ID](https://grafana.com/docs/grafana/latest/developer-resources/api-reference/http-api/annotations/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `annotation_id` | path | `number` | yes | The annotation ID. |
