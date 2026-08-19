# Get Page Insights with Facebook

Get analytics and metrics for a Page.

## Endpoint

- **Method:** `GET`
- **Path:** `/:pageId/insights`
- **Base URL:** `https://graph.facebook.com/v25.0`
- **Official documentation:** [Get Page Insights](https://developers.facebook.com/docs/graph-api/reference/v25.0/insights)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `breakdown` | query | `string` | no | A valid breakdown for an insights endpoint. |
| `pageId` | path | `string` | yes | — |
| `date_preset` | query | `list<string>` | no | enum: today, yesterday, this_month, last_month, this_quarter, maximum, data_maximum, last_3d, last_7d, last_14d, last_28d, last_30d, last_90d, last_week_mon_sun, last_week_sun_sat, last_quarter, last_year, this_week_mon_today, this_week_sun_today, this_year |
| `metric` | query | `list<string>` | no | A valid metric for an insights endpoint.  This is not an exhaustive list of available metrics. For a full list of available metrics, refer to [Page Insights](https://developers.facebook.com/docs/graph-api/reference/v25.0/insights). Send multiple values as a array. |
| `period` | query | `list<string>` | no | enum: day week days_28 month lifetime total_over_range |
| `since` | query | `string` | no | datetime |
| `until` | query | `string` | no | datetime |
| `show_description_from_api_doc` | query | `boolean` | no | Default value: false show_description_from_api_doc |
| `pageAccessToken` | body | `string` | no | — |
