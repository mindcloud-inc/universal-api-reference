# Socialbu: Get Supported Post Options

Retrieves supported posting options for SocialBu accounts.

```
GET https://connect.mindcloud.co/v1/universal/socialbu/latest/actions/get-supported-post-options
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Socialbu `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/socialbu/latest/actions/get-supported-post-options?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/socialbu/latest/actions/get-supported-post-options?${params}`, {
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
      "account_id": 1,
      "items": [
        {}
      ],
      "options": {},
      "provider": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `account_id` | number |  |
| `items` | array<object> |  |
| `options` | object |  |
| `provider` | string |  |

## Native endpoint

Through the native Socialbu API, this operation is `GET /posts/supported-options` (base URL `https://socialbu.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-supported-post-options.md) for the provider-specific parameters and requirements.

