# Rocketadmin: Get API Key



```
GET https://connect.mindcloud.co/v1/universal/rocketadmin/latest/actions/get-api-key
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Rocketadmin `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/rocketadmin/latest/actions/get-api-key?connectionId=$CONNECTION_ID&apiKeyId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "apiKeyId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/rocketadmin/latest/actions/get-api-key?${params}`, {
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
| `apiKeyId` | string | yes | Rocketadmin API key identifier from the path. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "message": "string",
      "path": "string",
      "statusCode": 1,
      "timestamp": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `message` | string |  |
| `path` | string |  |
| `statusCode` | number |  |
| `timestamp` | string |  |

## Native endpoint

Through the native Rocketadmin API, this operation is `GET /apikey/:apiKeyId` (base URL `https://app.rocketadmin.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-api-key.md) for the provider-specific parameters and requirements.

