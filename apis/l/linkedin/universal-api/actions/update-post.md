# LinkedIn: Update Post

Updates an existing post in LinkedIn.

```
PUT https://connect.mindcloud.co/v1/universal/linkedin/latest/actions/update-post
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a LinkedIn `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/linkedin/latest/actions/update-post" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "encodedPostUrn": "urn%3Ali%3AugcPost%3A7108134504928301056",
  "patch": "[object Object]"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/linkedin/latest/actions/update-post', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "encodedPostUrn": "urn%3Ali%3AugcPost%3A7108134504928301056",
    "patch": "[object Object]"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `encodedPostUrn` | string | yes | Percent-encoded post URN path segment. Example: `urn%3Ali%3AugcPost%3A7108134504928301056`. |
| `patch` | object | yes | Partial update patch object, for example {"$set": {...}}. Example: `[object Object]`. |

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
| `value` | string | Endpoint returned an empty response body (204 No Content). |

## Native endpoint

Through the native LinkedIn API, this operation is `POST /rest/posts/:encodedPostUrn` (base URL `https://api.linkedin.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-post.md) for the provider-specific parameters and requirements.

