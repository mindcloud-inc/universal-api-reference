# Bluesky: Get Starter Pack

Retrieves details for a specific Bluesky starter pack.

```
GET https://connect.mindcloud.co/v1/universal/bluesky/latest/actions/get-starter-pack
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Bluesky `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bluesky/latest/actions/get-starter-pack?connectionId=$CONNECTION_ID&starterPack=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "starterPack": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/bluesky/latest/actions/get-starter-pack?${params}`, {
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
| `starterPack` | string | yes | AT-URI of the starter pack to inspect. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "starterPack": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `starterPack` | object |  |

## Native endpoint

Through the native Bluesky API, this operation is `GET /xrpc/app.bsky.graph.getStarterPack` (base URL `{{credentials.pdsUrl}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-starter-pack.md) for the provider-specific parameters and requirements.

