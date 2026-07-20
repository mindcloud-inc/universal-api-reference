# Reamaze: List Channels



```
GET https://connect.mindcloud.co/v1/universal/reamaze/latest/actions/list-channels
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Reamaze `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/reamaze/latest/actions/list-channels?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/reamaze/latest/actions/list-channels?${params}`, {
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
| `channel` | string | no | `channel` with `email`, `facebook`, `twitter`, or `chat` will show only channels by the respective types. |
| `email` | string | no | `channel` with `email`, `facebook`, `twitter`, or `chat` will show only channels by the respective types. |
| `facebook` | string | no | `channel` with `email`, `facebook`, `twitter`, or `chat` will show only channels by the respective types. |
| `twitter` | string | no | `channel` with `email`, `facebook`, `twitter`, or `chat` will show only channels by the respective types. |
| `chat` | string | no | `channel` with `email`, `facebook`, `twitter`, or `chat` will show only channels by the respective types. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "channels": [
        {}
      ],
      "totalCount": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `channels` | array<object> |  |
| `totalCount` | number |  |

## Native endpoint

Through the native Reamaze API, this operation is `GET /channels` (base URL `https://{{credentials.brand}}.reamaze.io/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-channels.md) for the provider-specific parameters and requirements.

