# Assembly.com: List App Installs

Retrieves app installs in the current Assembly.com workspace.

```
GET https://connect.mindcloud.co/v1/universal/assemblycom/latest/actions/list-app-installs
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Assembly.com `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/assemblycom/latest/actions/list-app-installs?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/assemblycom/latest/actions/list-app-installs?${params}`, {
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
      "appId": "string",
      "displayName": "Ava Chen",
      "id": "string",
      "object": "string",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `appId` | string |  |
| `displayName` | string |  |
| `id` | string |  |
| `object` | string |  |
| `type` | string |  |

## Native endpoint

Through the native Assembly.com API, this operation is `GET /installs` (base URL `https://api.assembly.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-app-installs.md) for the provider-specific parameters and requirements.

