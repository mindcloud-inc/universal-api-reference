# Swarm: Get Profile Posts

Retrieves profile posts from Swarm by LinkedIn ID.

```
GET https://connect.mindcloud.co/v1/universal/swarm/latest/actions/get-profile-posts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Swarm `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/swarm/latest/actions/get-profile-posts?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/swarm/latest/actions/get-profile-posts?${params}`, {
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
| `linkedinID` | string | no | LinkedIn profile slug to retrieve posts for. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "paginationToken": "string",
      "posts": [
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
| `paginationToken` | string |  |
| `posts` | array<object> |  |

## Native endpoint

Through the native Swarm API, this operation is `GET /social/profile/posts` (base URL `https://bee.theswarm.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-profile-posts.md) for the provider-specific parameters and requirements.

