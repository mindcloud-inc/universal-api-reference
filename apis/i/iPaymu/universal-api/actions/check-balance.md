# iPaymu: Check Balance

Check your iPaymu account balance.

```
GET https://connect.mindcloud.co/v1/universal/iPaymu/latest/actions/check-balance
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a iPaymu `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/iPaymu/latest/actions/check-balance?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/iPaymu/latest/actions/check-balance?${params}`, {
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
      "memberBalance": 1,
      "merchantBalance": 1,
      "va": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `memberBalance` | number |  |
| `merchantBalance` | number |  |
| `va` | string |  |

## Native endpoint

Through the native iPaymu API, this operation is `POST /balance` (base URL `https://my.ipaymu.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/check-balance.md) for the provider-specific parameters and requirements.

