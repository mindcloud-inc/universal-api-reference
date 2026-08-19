# Facebook: Get Page Insights

Get analytics and metrics for a Page.

```
GET https://connect.mindcloud.co/v1/universal/facebook/latest/actions/get-page-insights
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Facebook `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/facebook/latest/actions/get-page-insights?connectionId=$CONNECTION_ID&pageId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "pageId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/facebook/latest/actions/get-page-insights?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `breakdown` | string | no | A valid breakdown for an insights endpoint. |
| `pageId` | string | yes |  |
| `datePreset` | list<string> | no | enum: today, yesterday, this_month, last_month, this_quarter, maximum, data_maximum, last_3d, last_7d, last_14d, last_28d, last_30d, last_90d, last_week_mon_sun, last_week_sun_sat, last_quarter, last_year, this_week_mon_today, this_week_sun_today, this_year |
| `metric` | list<string> | no | A valid metric for an insights endpoint. This is not an exhaustive list of available metrics. For a full list of available metrics, refer to [Page Insights](https://developers.facebook.com/docs/graph-api/reference/v25.0/insights). Accepts multiple values as an array. |
| `period` | list<string> | no | enum: day week days_28 month lifetime total_over_range |
| `since` | string | no | datetime |
| `until` | string | no | datetime |
| `pageAccessToken` | string | no |  |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `showApiDescription` | boolean | no | Default value: false show_description_from_api_doc |

## Response

```json
{
  "success": true,
  "data": [
    {
      "description": "string",
      "id": "string",
      "name": "Ava Chen",
      "period": "string",
      "title": "string",
      "values": [
        {
          "endTime": "string",
          "value": 1
        }
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `description` | string |  |
| `id` | string |  |
| `name` | string |  |
| `period` | string |  |
| `title` | string |  |
| `values[].endTime` | string |  |
| `values[].value` | number |  |

## Native endpoint

Through the native Facebook API, this operation is `GET /:pageId/insights` (base URL `https://graph.facebook.com/v25.0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-page-insights.md) for the provider-specific parameters and requirements.

