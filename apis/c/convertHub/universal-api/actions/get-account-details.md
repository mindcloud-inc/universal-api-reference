# ConvertHub: Get Account Details

Retrieves account credits and plan details from ConvertHub.

```
GET https://connect.mindcloud.co/v1/universal/convertHub/latest/actions/get-account-details
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ConvertHub `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/convertHub/latest/actions/get-account-details?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/convertHub/latest/actions/get-account-details?${params}`, {
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
      "credits_remaining": 1,
      "plan": {
        "credits": 1,
        "file_size_limit": 1,
        "file_size_limit_mb": 1,
        "name": "Ava Chen",
        "price": 1
      },
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `credits_remaining` | number |  |
| `plan` | object |  |
| `plan.credits` | number |  |
| `plan.file_size_limit` | number |  |
| `plan.file_size_limit_mb` | number |  |
| `plan.name` | string |  |
| `plan.price` | number |  |
| `success` | boolean |  |

## Native endpoint

Through the native ConvertHub API, this operation is `GET /v2/account` (base URL `https://api.converthub.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-account-details.md) for the provider-specific parameters and requirements.

