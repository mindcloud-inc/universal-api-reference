# Weberlo: Get UTM Channel

Retrieves a UTM channel from Weberlo.

```
GET https://connect.mindcloud.co/v1/universal/weberlo/latest/actions/get-utm-channel
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Weberlo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/weberlo/latest/actions/get-utm-channel?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/weberlo/latest/actions/get-utm-channel?${params}`, {
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
| `id` | string | yes | UTM channel ID. |

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

Through the native Weberlo API, this operation is `GET /channel-utm/:id` (base URL `https://connect.weberlo.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-utm-channel.md) for the provider-specific parameters and requirements.

