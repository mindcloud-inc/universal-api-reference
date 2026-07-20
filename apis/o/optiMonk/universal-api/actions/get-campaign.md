# OptiMonk: Get Campaign

Retrieves a campaign from OptiMonk.

```
GET https://connect.mindcloud.co/v1/universal/optiMonk/latest/actions/get-campaign
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a OptiMonk `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/optiMonk/latest/actions/get-campaign?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/optiMonk/latest/actions/get-campaign?${params}`, {
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
| `id` | number | yes | The OptiMonk campaign ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "conversionRates": {},
      "conversions": {},
      "id": 1,
      "impressions": {},
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
| `conversionRates` | object |  |
| `conversions` | object |  |
| `id` | number |  |
| `impressions` | object |  |
| `name` | string |  |
| `status` | string |  |
| `variants` | array<object> |  |

## Native endpoint

Through the native OptiMonk API, this operation is `GET /campaigns/{id}` (base URL `https://api.optimonk.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-campaign.md) for the provider-specific parameters and requirements.

