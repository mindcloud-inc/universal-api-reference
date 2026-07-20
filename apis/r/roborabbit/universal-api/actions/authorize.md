# Roborabbit: Authorize



```
GET https://connect.mindcloud.co/v1/universal/roborabbit/latest/actions/authorize
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Roborabbit `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/roborabbit/latest/actions/authorize?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/roborabbit/latest/actions/authorize?${params}`, {
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
      "message": "string",
      "workspace": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `message` | string | Authorization status message from the Roborabbit auth check endpoint. |
| `workspace` | string | Workspace name associated with the provided API key. |

## Native endpoint

Through the native Roborabbit API, this operation is `GET /v1/auth` (base URL `https://api.roborabbit.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/authorize.md) for the provider-specific parameters and requirements.

