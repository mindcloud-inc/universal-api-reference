# Loops: Test API Key

Retrieves API key validity details from Loops.

```
GET https://connect.mindcloud.co/v1/universal/loops/latest/actions/test-api-key
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Loops `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/loops/latest/actions/test-api-key?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/loops/latest/actions/test-api-key?${params}`, {
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
      "success": true,
      "teamName": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `success` | boolean |  |
| `teamName` | string |  |

## Native endpoint

Through the native Loops API, this operation is `GET /api-key` (base URL `https://app.loops.so/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/test-api-key.md) for the provider-specific parameters and requirements.

