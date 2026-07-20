# ThriveDesk: List Installed Apps



```
GET https://connect.mindcloud.co/v1/universal/thriveDesk/latest/actions/list-installed-apps
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ThriveDesk `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/thriveDesk/latest/actions/list-installed-apps?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/thriveDesk/latest/actions/list-installed-apps?${params}`, {
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
      "data": [
        {}
      ],
      "id": "string",
      "message": "string",
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | array<object> | Returned collection. |
| `id` | string | Resource identifier when returned. |
| `message` | string | Response message. |
| `success` | boolean | Whether the operation succeeded. |

## Native endpoint

Through the native ThriveDesk API, this operation is `GET /v1/installed-apps` (base URL `https://api.thrivedesk.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-installed-apps.md) for the provider-specific parameters and requirements.

