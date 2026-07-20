# OTO: List Pickup Locations

Retrieves pickup locations from the OTO API.

```
GET https://connect.mindcloud.co/v1/universal/oTO/latest/actions/list-pickup-locations
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a OTO `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/oTO/latest/actions/list-pickup-locations?connectionId=$CONNECTION_ID&minDate=2024-08-01" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "minDate": "2024-08-01"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/oTO/latest/actions/list-pickup-locations?${params}`, {
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
| `minDate` | date | yes | Earliest date to include when listing pickup locations, in YYYY-MM-DD format. Default: `2024-08-01`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "branches": [
        {}
      ],
      "success": true,
      "warehouses": [
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
| `branches` | array<object> |  |
| `success` | boolean |  |
| `warehouses` | array<object> |  |

## Native endpoint

Through the native OTO API, this operation is `GET /getPickupLocationList` (base URL `https://api.tryoto.com/rest/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-pickup-locations.md) for the provider-specific parameters and requirements.

