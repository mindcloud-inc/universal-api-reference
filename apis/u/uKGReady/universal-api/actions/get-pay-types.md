# UKG Ready: Get Pay Types



```
GET https://connect.mindcloud.co/v1/universal/uKGReady/latest/actions/get-pay-types
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a UKG Ready `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/uKGReady/latest/actions/get-pay-types?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/uKGReady/latest/actions/get-pay-types?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "payTypes": [
        {
          "id": 1,
          "name": "Ava Chen",
          "orderIndex": 1
        }
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `payTypes[].id` | number |  |
| `payTypes[].name` | string |  |
| `payTypes[].orderIndex` | number |  |

## Native endpoint

Through the native UKG Ready API, this operation is `GET /v1/employee/accrual-balances` (base URL `https://{{credentials.hostname}}/ta/rest`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-pay-types.md) for the provider-specific parameters and requirements.

