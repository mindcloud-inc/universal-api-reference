# Goodbarber eCommerce: Get Page Views Per Week Day



```
GET https://connect.mindcloud.co/v1/universal/goodbarberECommerce/latest/actions/get-page-views-per-week-day
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Goodbarber eCommerce `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/goodbarberECommerce/latest/actions/get-page-views-per-week-day?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/goodbarberECommerce/latest/actions/get-page-views-per-week-day?${params}`, {
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

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `endDate` | string | no | End date (included) with format %Y-%m-%d . Defaults to yesterday. |
| `startDate` | string | no | Start date (included) with format %Y-%m-%d . Defaults to one month ago. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "Friday": 1,
      "Monday": 1,
      "Saturday": 1,
      "Sunday": 1,
      "Thursday": 1,
      "Tuesday": 1,
      "Wednesday": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `Friday` | number | <div class="field_description">Total number of pages viewed on fridays during the specified time interval.</div> |
| `Monday` | number | <div class="field_description">Total number of pages viewed on mondays during the specified time interval.</div> |
| `Saturday` | number | <div class="field_description">Total number of pages viewed on saturdays during the specified time interval.</div> |
| `Sunday` | number | <div class="field_description">Total number of pages viewed on sundays during the specified time interval.</div> |
| `Thursday` | number | <div class="field_description">Total number of pages viewed on thursdays during the specified time interval.</div> |
| `Tuesday` | number | <div class="field_description">Total number of pages viewed on tuesdays during the specified time interval.</div> |
| `Wednesday` | number | <div class="field_description">Total number of pages viewed on wednesdays during the specified time interval.</div> |

## Native endpoint

Through the native Goodbarber eCommerce API, this operation is `GET /publicapi/v2/general/stats/:webzine_id/page_views_per_week_day/` (base URL `https://commerce.goodbarber.dev`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-page-views-per-week-day.md) for the provider-specific parameters and requirements.

