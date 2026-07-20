# Socket: Get Integration Events

Retrieves organization integration events from Socket.

```
GET https://connect.mindcloud.co/v1/universal/socket/latest/actions/get-integration-events
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Socket `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/socket/latest/actions/get-integration-events?connectionId=$CONNECTION_ID&integrationId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "integrationId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/socket/latest/actions/get-integration-events?${params}`, {
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
| `integrationId` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "items": [
        [
          {}
        ]
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `items[]` | array<object> |  |
| `items[].createdAt` | string |  |
| `items[].error` | string |  |
| `items[].id` | string |  |
| `items[].integrationId` | string |  |
| `items[].payload` | object |  |
| `items[].retryInfo` | array<object> |  |
| `items[].retryInfo[]` | object |  |
| `items[].retryInfo[].error` | string |  |
| `items[].retryInfo[].sentAt` | string |  |
| `items[].retryInfo[].statusCode` | number |  |
| `items[].sentAt` | string |  |
| `items[].statusCode` | number |  |
| `items[].type` | string |  |
| `items[].updatedAt` | string |  |

## Native endpoint

Through the native Socket API, this operation is `GET /orgs/:org_slug/settings/integrations/:integration_id/events` (base URL `https://api.socket.dev/v0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-integration-events.md) for the provider-specific parameters and requirements.

