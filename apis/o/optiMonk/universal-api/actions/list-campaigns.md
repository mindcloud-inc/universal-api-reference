# OptiMonk: List Campaigns

Retrieves a list of campaigns from OptiMonk.

```
GET https://connect.mindcloud.co/v1/universal/optiMonk/latest/actions/list-campaigns
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a OptiMonk `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/optiMonk/latest/actions/list-campaigns?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/optiMonk/latest/actions/list-campaigns?${params}`, {
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
| `page` | number | no | Pagination index. Starts at 1. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "conversionRate": 1,
      "conversions": 1,
      "id": 1,
      "impressions": 1,
      "name": "Ava Chen",
      "status": "string",
      "variants": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `conversionRate` | number |  |
| `conversions` | number |  |
| `id` | number |  |
| `impressions` | number |  |
| `name` | string |  |
| `status` | string |  |
| `variants` | array<object> |  |

## Native endpoint

Through the native OptiMonk API, this operation is `GET /campaigns/` (base URL `https://api.optimonk.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-campaigns.md) for the provider-specific parameters and requirements.

