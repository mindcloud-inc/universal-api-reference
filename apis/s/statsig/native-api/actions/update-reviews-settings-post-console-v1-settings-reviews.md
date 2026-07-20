# Update Reviews Settings with Statsig

Updates review settings in Statsig.

## Endpoint

- **Method:** `POST`
- **Path:** `/console/v1/settings/reviews`
- **Base URL:** `https://statsigapi.net`
- **API:** rest
- **Official documentation:** [Update Reviews Settings](https://docs.statsig.com/api-reference/settings/update-reviews-settings)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `is_config_review_required` | body | `boolean` | yes | Request body field. |
| `is_metric_review_required` | body | `boolean` | yes | Request body field. |
| `is_metric_review_required_on_verified_only` | body | `boolean` | yes | Request body field. |
| `is_whn_analysis_only_review_required` | body | `boolean` | no | Request body field. |
| `is_whn_source_review_required` | body | `boolean` | no | Request body field. |
