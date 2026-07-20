# NobelSMS: List Balances

Retrieves balances from NobelSMS.

```
GET https://connect.mindcloud.co/v1/universal/nobelSMS/latest/actions/list-balances
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a NobelSMS `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/nobelSMS/latest/actions/list-balances?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/nobelSMS/latest/actions/list-balances?${params}`, {
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
| `carId` | number | no | Carrier ID (for System owner users only). |
| `description` | string | no | Account description filter. |
| `direction` | number | no | Account direction. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "balance": 1,
      "balance_updated": "string",
      "car_id": 1,
      "currency_code": "string",
      "descr": "string",
      "id": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `balance` | number |  |
| `balance_updated` | string |  |
| `car_id` | number |  |
| `currency_code` | string |  |
| `descr` | string |  |
| `id` | number |  |

## Native endpoint

Through the native NobelSMS API, this operation is `GET /balance` (base URL `https://api.nobelsms.com/rest`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-balances.md) for the provider-specific parameters and requirements.

