# Swarm: Get Post Reactions

Retrieves reactions for a post from Swarm.

```
GET https://connect.mindcloud.co/v1/universal/swarm/latest/actions/get-post-reactions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Swarm `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/swarm/latest/actions/get-post-reactions?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/swarm/latest/actions/get-post-reactions?${params}`, {
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
| `postUrn` | string | no | LinkedIn post URN used in the route path. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "pages": 1,
      "results": [
        {}
      ],
      "totalResults": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `pages` | number |  |
| `results` | array<object> |  |
| `totalResults` | number |  |

## Native endpoint

Through the native Swarm API, this operation is `GET /social/post/:postUrn/reactions` (base URL `https://bee.theswarm.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-post-reactions.md) for the provider-specific parameters and requirements.

