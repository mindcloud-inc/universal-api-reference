# TgBooster: Get Reports

Retrieves custom campaign reports from a TgBooster cabinet.

```
GET https://connect.mindcloud.co/v1/universal/tgBooster/latest/actions/get-reports
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a TgBooster `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/tgBooster/latest/actions/get-reports?connectionId=$CONNECTION_ID&cabinetId=242" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "cabinetId": "242"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/tgBooster/latest/actions/get-reports?${params}`, {
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
| `cabinetId` | number | yes | Cabinet ID returned by List Cabinets. Example: `242`. |
| `groups[date][day]` | boolean | no | Group report rows by day. Default: `true`. |
| `groups[ads][company]` | boolean | no | Group report rows by campaign. |
| `filters[dates][]` | array<date> | no | Two report dates: start date and end date. Accepts multiple values as an array. Example: `2023-03-01, 2023-09-10`. |
| `metrics[views]` | boolean | no | Include views metric. Default: `true`. |
| `metrics[clicks]` | boolean | no | Include clicks metric. Default: `true`. |
| `metrics[joins]` | boolean | no | Include joins metric. Default: `true`. |
| `metrics[spent]` | boolean | no | Include spent metric. Default: `true`. |
| `metrics[ctr]` | boolean | no | Include CTR metric. Default: `true`. |
| `metrics[cv]` | boolean | no | Include conversion from views to joins. Default: `true`. |
| `metrics[cpc]` | boolean | no | Include CPC metric. Default: `true`. |
| `metrics[cps]` | boolean | no | Include CPS metric. Default: `true`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `groups[date][week]` | boolean | no | Group report rows by week. |
| `groups[ads][ad]` | boolean | no | Group report rows by ad. |
| `groups[ads][adUrl]` | boolean | no | Group report rows by ad URL. |
| `filters[company][]` | array<number> | no | Campaign IDs to include in the report. Accepts multiple values as an array. Example: `1, 2`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "date_day": "2026-05-07T12:00:00.000Z",
      "metric_clicks": "string",
      "metric_cpc": 1,
      "metric_cps": 1,
      "metric_ctr": 1,
      "metric_cv": 1,
      "metric_joins": "string",
      "metric_spent": "string",
      "metric_views": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `date_day` | date | Report day when grouped by day. |
| `metric_clicks` | string | Clicks metric as returned by TgBooster. |
| `metric_cpc` | number | CPC metric. |
| `metric_cps` | number | CPS metric. |
| `metric_ctr` | number | CTR metric. |
| `metric_cv` | number | Conversion metric from views to joins. |
| `metric_joins` | string | Joins metric as returned by TgBooster. |
| `metric_spent` | string | Spent metric as returned by TgBooster. |
| `metric_views` | string | Views metric as returned by TgBooster. |

## Native endpoint

Through the native TgBooster API, this operation is `POST /cabinet/{CabinetId}/reports` (base URL `https://api.tgbooster.ru/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-reports.md) for the provider-specific parameters and requirements.

