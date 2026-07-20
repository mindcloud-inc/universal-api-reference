# Leantime: Get Client



```
GET https://connect.mindcloud.co/v1/universal/leantime/latest/actions/get-client
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Leantime `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/leantime/latest/actions/get-client?connectionId=$CONNECTION_ID&clientId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "clientId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/leantime/latest/actions/get-client?${params}`, {
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
| `clientId` | number | yes | The Leantime client id. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "city": "string",
      "country": "string",
      "email": "ava@example.com",
      "id": 1,
      "internet": "string",
      "name": "Ava Chen",
      "numberOfProjects": 1,
      "phone": "string",
      "state": "string",
      "street": "string",
      "zip": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `city` | string |  |
| `country` | string |  |
| `email` | string |  |
| `id` | number |  |
| `internet` | string |  |
| `name` | string |  |
| `numberOfProjects` | number |  |
| `phone` | string |  |
| `state` | string |  |
| `street` | string |  |
| `zip` | number |  |

## Native endpoint

Through the native Leantime API, this operation is `POST /` (base URL `{{credentials.workspaceUrl}}/api/jsonrpc`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-client.md) for the provider-specific parameters and requirements.

