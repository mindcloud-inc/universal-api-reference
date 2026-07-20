# Weberlo: Update UTM Channel

Updates a UTM channel in Weberlo.

```
PUT https://connect.mindcloud.co/v1/universal/weberlo/latest/actions/update-utm-channel
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Weberlo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/weberlo/latest/actions/update-utm-channel" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/weberlo/latest/actions/update-utm-channel', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes | UTM channel ID. |
| `name` | string | no | Updated UTM channel name. Example: `Updated UTM Channel`. |
| `icon` | string | no | Updated UTM channel icon URL. Example: `https://example.com/utm-channel-updated.png`. |
| `conditions[]` | array<object> | no | Updated UTM matching conditions array. Example: `[object Object]`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "conditions": [
        {}
      ],
      "icon": "string",
      "id": "string",
      "name": "Ava Chen",
      "workspaceId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `conditions` | array<object> |  |
| `icon` | string |  |
| `id` | string |  |
| `name` | string |  |
| `workspaceId` | string |  |

## Native endpoint

Through the native Weberlo API, this operation is `PATCH /channel-utm/:id` (base URL `https://connect.weberlo.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-utm-channel.md) for the provider-specific parameters and requirements.

