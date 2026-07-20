# LinkedIn: Delete Post

Deletes an existing post from LinkedIn.

```
DELETE https://connect.mindcloud.co/v1/universal/linkedin/latest/actions/delete-post
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a LinkedIn `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/linkedin/latest/actions/delete-post?connectionId=$CONNECTION_ID&encodedPostUrn=urn%253Ali%253AugcPost%253A7108134504928301056" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "encodedPostUrn": "urn%3Ali%3AugcPost%3A7108134504928301056"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/linkedin/latest/actions/delete-post?${params}`, {
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
| `encodedPostUrn` | string | yes | Percent-encoded post URN path segment. Example: `urn%3Ali%3AugcPost%3A7108134504928301056`. |

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

Through the native LinkedIn API, this operation is `DELETE /rest/posts/:encodedPostUrn` (base URL `https://api.linkedin.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-post.md) for the provider-specific parameters and requirements.

