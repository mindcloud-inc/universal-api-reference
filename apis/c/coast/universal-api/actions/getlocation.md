# Coast: Get Location By ID



```
GET https://connect.mindcloud.co/v1/universal/coast/latest/actions/getlocation
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Coast `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/coast/latest/actions/getlocation?connectionId=$CONNECTION_ID&locationId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "locationId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/coast/latest/actions/getlocation?${params}`, {
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
| `locationId` | string | yes | Coast location ID of the location to retrieve. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "accountId": "string",
      "city": {},
      "id": "string",
      "name": "Ava Chen",
      "state": {},
      "streetAddress": {},
      "streetAddress2": {},
      "zip": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accountId` | string |  |
| `city` | object |  |
| `id` | string |  |
| `name` | string |  |
| `state` | object |  |
| `streetAddress` | object |  |
| `streetAddress2` | object |  |
| `zip` | object |  |

## Native endpoint

Through the native Coast API, this operation is `GET /v2/locations/:locationId` (base URL `https://public.coastpay.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/getlocation.md) for the provider-specific parameters and requirements.

