# Bluesky: Get List

Retrieves details for a specific Bluesky list.

```
GET https://connect.mindcloud.co/v1/universal/bluesky/latest/actions/get-list
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Bluesky `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bluesky/latest/actions/get-list?connectionId=$CONNECTION_ID&list=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "list": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/bluesky/latest/actions/get-list?${params}`, {
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
| `list` | string | yes | AT-URI of the list to inspect. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "cursor": "string",
      "items": [
        {}
      ],
      "list": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `cursor` | string |  |
| `items` | array<object> |  |
| `list` | object |  |

## Native endpoint

Through the native Bluesky API, this operation is `GET /xrpc/app.bsky.graph.getList` (base URL `{{credentials.pdsUrl}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-list.md) for the provider-specific parameters and requirements.

