# Bluesky: Get Actor Starter Packs

Retrieves Bluesky starter packs created by a specific actor.

```
GET https://connect.mindcloud.co/v1/universal/bluesky/latest/actions/get-actor-starter-packs
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Bluesky `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bluesky/latest/actions/get-actor-starter-packs?connectionId=$CONNECTION_ID&actor=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "actor": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/bluesky/latest/actions/get-actor-starter-packs?${params}`, {
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
| `actor` | string | yes | Handle or DID whose starter packs you want to inspect. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "cursor": "string",
      "starterPacks": [
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
| `starterPacks` | array<object> |  |

## Native endpoint

Through the native Bluesky API, this operation is `GET /xrpc/app.bsky.graph.getActorStarterPacks` (base URL `{{credentials.pdsUrl}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-actor-starter-packs.md) for the provider-specific parameters and requirements.

