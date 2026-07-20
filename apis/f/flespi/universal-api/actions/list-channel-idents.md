# Flespi: List channel idents



```
GET https://connect.mindcloud.co/v1/universal/flespi/latest/actions/list-channel-idents
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Flespi `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/flespi/latest/actions/list-channel-idents?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/flespi/latest/actions/list-channel-idents?${params}`, {
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
      "channel_id": 1,
      "ident": "string",
      "last_active": "2026-05-07T12:00:00.000Z",
      "result": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `channel_id` | number | Channel ID. |
| `ident` | string | Channel ident. |
| `last_active` | date | Last active timestamp. |
| `result` | array<object> | Flespi response result items. |

## Native endpoint

Through the native Flespi API, this operation is `GET /gw/channels/all/idents/all` (base URL `https://flespi.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-channel-idents.md) for the provider-specific parameters and requirements.

