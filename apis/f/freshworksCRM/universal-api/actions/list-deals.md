# Freshworks CRM: List Deals

Retrieves deals from a view in Freshworks CRM.

```
GET https://connect.mindcloud.co/v1/universal/freshworksCRM/latest/actions/list-deals
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Freshworks CRM `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/freshworksCRM/latest/actions/list-deals?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/freshworksCRM/latest/actions/list-deals?${params}`, {
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
| `viewId` | number | no | Numeric view identifier used for list queries. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "deals": [
        {
          "age": 1,
          "amount": "string",
          "closed_date": "2026-05-07T12:00:00.000Z",
          "created_at": "2026-05-07T12:00:00.000Z",
          "custom_field": {
            "cf_number_of_agents": 1
          },
          "expected_close": "2026-05-07T12:00:00.000Z",
          "id": 1,
          "name": "Ava Chen",
          "probability": 1,
          "stage_updated_time": "2026-05-07T12:00:00.000Z",
          "updated_at": "2026-05-07T12:00:00.000Z"
        }
      ],
      "meta": {
        "total": 1
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `deals[].age` | number | Deal age. |
| `deals[].amount` | string | Deal amount. |
| `deals[].closed_date` | date | Closed date. |
| `deals[].created_at` | date | Created timestamp. |
| `deals[].custom_field.cf_number_of_agents` | number | Custom number-of-agents field. |
| `deals[].expected_close` | date | Expected close date. |
| `deals[].id` | number | Deal identifier. |
| `deals[].name` | string | Deal name. |
| `deals[].probability` | number | Deal probability. |
| `deals[].stage_updated_time` | date | Stage updated timestamp. |
| `deals[].updated_at` | date | Updated timestamp. |
| `meta.total` | number | Total deals count. |

## Native endpoint

Through the native Freshworks CRM API, this operation is `GET api/deals/view/:view_id` (base URL `https://{{credentials.bundleAlias}}`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-deals.md) for the provider-specific parameters and requirements.

