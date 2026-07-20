# LinkedIn: Create Post

Creates a new post in LinkedIn.

```
POST https://connect.mindcloud.co/v1/universal/linkedin/latest/actions/create-post
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a LinkedIn `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/linkedin/latest/actions/create-post" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "author": "urn:li:organization:5515715",
  "commentary": "Sample text post created from LinkedIn API"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/linkedin/latest/actions/create-post', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "author": "urn:li:organization:5515715",
    "commentary": "Sample text post created from LinkedIn API"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `author` | string | yes | Author URN such as urn:li:organization:{id} or urn:li:person:{id}. Example: `urn:li:organization:5515715`. |
| `commentary` | string | yes | Text content for the post commentary. Example: `Sample text post created from LinkedIn API`. |
| `visibility` | list | no | Who can see the post. One of: `CONNECTIONS`, `CONTAINER`, `LOGGED_IN`, `PUBLIC`, `TARGETED_ENTITIES`. Default: `PUBLIC`. Example: `PUBLIC`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "value": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `value` | string | LinkedIn returns the created post identifier in the x-restli-id response header and no response body for this successful mutation. |

## Native endpoint

Through the native LinkedIn API, this operation is `POST /rest/posts` (base URL `https://api.linkedin.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-post.md) for the provider-specific parameters and requirements.

