# TgBooster: List Campaigns

Retrieves campaigns from a specific TgBooster cabinet.

```
GET https://connect.mindcloud.co/v1/universal/tgBooster/latest/actions/list-campaigns
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a TgBooster `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/tgBooster/latest/actions/list-campaigns?connectionId=$CONNECTION_ID&cabinetId=242" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "cabinetId": "242"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/tgBooster/latest/actions/list-campaigns?${params}`, {
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

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `filters[startDate]` | date | no | Start date for campaign statistics filtering. Example: `2023-03-01`. |
| `filters[finishDate]` | date | no | Finish date for campaign statistics filtering. Example: `2023-09-10`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "ads_active_count": 1,
      "ads_count": 1,
      "ads_sum_budget": "string",
      "cabinet_id": 1,
      "created_at": "2026-05-07T12:00:00.000Z",
      "id": 1,
      "name": "Ava Chen",
      "stat_clicks": "string",
      "stat_joins": "string",
      "stat_spent": "string",
      "stat_views": "string",
      "status_id": 1,
      "status": {
        "id": 1,
        "indicator": "string",
        "name": "Ava Chen"
      },
      "system": 1,
      "updated_at": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `ads_active_count` | number | Active ad count. |
| `ads_count` | number | Total ad count. |
| `ads_sum_budget` | string | Sum of ad budgets as returned by TgBooster. |
| `cabinet_id` | number | Parent cabinet ID. |
| `created_at` | date | Campaign creation timestamp. |
| `id` | number | Campaign ID. |
| `name` | string | Campaign name. |
| `stat_clicks` | string | Campaign clicks statistic as returned by TgBooster. |
| `stat_joins` | string | Campaign joins statistic as returned by TgBooster. |
| `stat_spent` | string | Campaign spent statistic as returned by TgBooster. |
| `stat_views` | string | Campaign views statistic as returned by TgBooster. |
| `status_id` | number | Campaign status ID. |
| `status.id` | number | Nested status ID. |
| `status.indicator` | string | Nested status indicator. |
| `status.name` | string | Nested status label. |
| `system` | number | System campaign flag. |
| `updated_at` | date | Campaign update timestamp. |

## Native endpoint

Through the native TgBooster API, this operation is `POST /cabinet/{CabinetId}/companies` (base URL `https://api.tgbooster.ru/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-campaigns.md) for the provider-specific parameters and requirements.

