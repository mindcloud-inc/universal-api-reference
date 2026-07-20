# Bluesky: Describe Server

Retrieves Bluesky server capabilities and account creation requirements.

```
GET https://connect.mindcloud.co/v1/universal/bluesky/latest/actions/describe-server
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Bluesky `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bluesky/latest/actions/describe-server?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/bluesky/latest/actions/describe-server?${params}`, {
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
      "availableUserDomains": [
        "string"
      ],
      "contact": {},
      "did": "string",
      "inviteCodeRequired": true,
      "links": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `availableUserDomains` | array<string> |  |
| `contact` | object |  |
| `did` | string |  |
| `inviteCodeRequired` | boolean |  |
| `links` | object |  |

## Native endpoint

Through the native Bluesky API, this operation is `GET /xrpc/com.atproto.server.describeServer` (base URL `{{credentials.pdsUrl}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/describe-server.md) for the provider-specific parameters and requirements.

