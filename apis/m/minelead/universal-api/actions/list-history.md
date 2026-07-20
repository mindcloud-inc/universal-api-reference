# Minelead: List History

Retrieves search history from your Minelead account.

```
GET https://connect.mindcloud.co/v1/universal/minelead/latest/actions/list-history
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Minelead `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/minelead/latest/actions/list-history?connectionId=$CONNECTION_ID&start=1&limit=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "start": "1",
  "limit": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/minelead/latest/actions/list-history?${params}`, {
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
| `start` | number | yes | History offset to start from. |
| `limit` | number | yes | Maximum number of history records to return. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "history": [
        {}
      ],
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `history` | array<object> |  |
| `status` | string |  |

## Native endpoint

Through the native Minelead API, this operation is `GET /history` (base URL `https://api.minelead.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-history.md) for the provider-specific parameters and requirements.

