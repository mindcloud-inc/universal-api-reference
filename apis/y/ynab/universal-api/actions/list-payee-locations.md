# YNAB: List Payee Locations

Retrieves payee locations from a YNAB plan.

```
GET https://connect.mindcloud.co/v1/universal/ynab/latest/actions/list-payee-locations
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a YNAB `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ynab/latest/actions/list-payee-locations?connectionId=$CONNECTION_ID&planId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "planId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/ynab/latest/actions/list-payee-locations?${params}`, {
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
| `planId` | string | yes | The id of the plan. You can also use last-used or default when enabled. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "deleted": true,
      "id": "string",
      "latitude": 1,
      "longitude": 1,
      "payeeId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `deleted` | boolean | Whether the payee location has been deleted. |
| `id` | string | The payee location ID. |
| `latitude` | number | The latitude for the payee location. |
| `longitude` | number | The longitude for the payee location. |
| `payeeId` | string | The associated payee ID. |

## Native endpoint

Through the native YNAB API, this operation is `GET /plans/:planId/payee_locations` (base URL `https://api.ynab.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-payee-locations.md) for the provider-specific parameters and requirements.

