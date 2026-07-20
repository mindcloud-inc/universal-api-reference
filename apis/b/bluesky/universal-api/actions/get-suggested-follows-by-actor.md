# Bluesky: Get Suggested Follows By Actor

Retrieves Bluesky follow suggestions similar to a specific actor.

```
GET https://connect.mindcloud.co/v1/universal/bluesky/latest/actions/get-suggested-follows-by-actor
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Bluesky `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bluesky/latest/actions/get-suggested-follows-by-actor?connectionId=$CONNECTION_ID&actor=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "actor": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/bluesky/latest/actions/get-suggested-follows-by-actor?${params}`, {
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
| `actor` | string | yes | Handle or DID to use for suggested follows. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "cursor": "string",
      "suggestions": [
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
| `cursor` | string |  |
| `suggestions` | array<object> |  |

## Native endpoint

Through the native Bluesky API, this operation is `GET /xrpc/app.bsky.graph.getSuggestedFollowsByActor` (base URL `{{credentials.pdsUrl}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-suggested-follows-by-actor.md) for the provider-specific parameters and requirements.

