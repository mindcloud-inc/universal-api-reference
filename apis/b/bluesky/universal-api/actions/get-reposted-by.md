# Bluesky: Get Reposted By

Retrieves accounts that reposted a specific Bluesky post.

```
GET https://connect.mindcloud.co/v1/universal/bluesky/latest/actions/get-reposted-by
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Bluesky `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bluesky/latest/actions/get-reposted-by?connectionId=$CONNECTION_ID&uri=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "uri": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/bluesky/latest/actions/get-reposted-by?${params}`, {
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
| `uri` | string | yes | AT-URI of the post whose reposts you want to inspect. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "cid": "string",
      "cursor": "string",
      "repostedBy": [
        {}
      ],
      "uri": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `cid` | string |  |
| `cursor` | string |  |
| `repostedBy` | array<object> |  |
| `uri` | string |  |

## Native endpoint

Through the native Bluesky API, this operation is `GET /xrpc/app.bsky.feed.getRepostedBy` (base URL `{{credentials.pdsUrl}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-reposted-by.md) for the provider-specific parameters and requirements.

