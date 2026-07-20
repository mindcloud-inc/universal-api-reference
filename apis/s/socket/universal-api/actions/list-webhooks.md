# Socket: List Webhooks

Retrieves configured organization webhooks from Socket.

```
GET https://connect.mindcloud.co/v1/universal/socket/latest/actions/list-webhooks
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Socket `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/socket/latest/actions/list-webhooks?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/socket/latest/actions/list-webhooks?${params}`, {
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
      "nextPage": 1,
      "results": [
        {
          "createdAt": "string",
          "description": "string",
          "events": [
            "string"
          ],
          "filters": {
            "repositoryIds": [
              "string"
            ]
          },
          "headers": {},
          "id": "string",
          "name": "Ava Chen",
          "secret": "string",
          "updatedAt": "string",
          "url": "https://example.com"
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
| `nextPage` | number |  |
| `results` | array<object> |  |
| `results[]` | object |  |
| `results[].createdAt` | string | The creation date of the webhook |
| `results[].description` | string | The description of the webhook |
| `results[].events` | array<string> |  |
| `results[].filters` | object |  |
| `results[].filters.repositoryIds` | array | Array of repository IDs |
| `results[].headers` | object | Custom headers to include in webhook requests |
| `results[].id` | string | The ID of the webhook |
| `results[].name` | string | The name of the webhook |
| `results[].secret` | string | The signing key used to sign webhook payloads |
| `results[].updatedAt` | string | The last update date of the webhook |
| `results[].url` | string | The URL where webhook events will be sent |

## Native endpoint

Through the native Socket API, this operation is `GET /orgs/:org_slug/webhooks` (base URL `https://api.socket.dev/v0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-webhooks.md) for the provider-specific parameters and requirements.

