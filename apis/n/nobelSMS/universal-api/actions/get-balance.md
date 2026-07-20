# NobelSMS: Get Balance

Retrieves a balance from NobelSMS by ID.

```
GET https://connect.mindcloud.co/v1/universal/nobelSMS/latest/actions/get-balance
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a NobelSMS `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/nobelSMS/latest/actions/get-balance?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/nobelSMS/latest/actions/get-balance?${params}`, {
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
| `id` | number | yes | Account ID. |

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

Through the native NobelSMS API, this operation is `GET /balance/:id` (base URL `https://api.nobelsms.com/rest`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-balance.md) for the provider-specific parameters and requirements.

