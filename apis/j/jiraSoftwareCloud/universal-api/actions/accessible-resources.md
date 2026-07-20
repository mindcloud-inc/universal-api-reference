# Jira Software Cloud: Accessible Resources

Retrieves accessible Jira Software Cloud sites for this token.

```
GET https://connect.mindcloud.co/v1/universal/jiraSoftwareCloud/latest/actions/accessible-resources
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Jira Software Cloud `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/jiraSoftwareCloud/latest/actions/accessible-resources?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/jiraSoftwareCloud/latest/actions/accessible-resources?${params}`, {
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
      "avatarUrl": "https://example.com",
      "id": "string",
      "name": "Ava Chen",
      "scopes": [
        "string"
      ],
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `avatarUrl` | string |  |
| `id` | string |  |
| `name` | string |  |
| `scopes[]` | string |  |
| `url` | string |  |

## Native endpoint

Through the native Jira Software Cloud API, this operation is `GET /oauth/token/accessible-resources` (base URL `https://api.atlassian.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/accessible-resources.md) for the provider-specific parameters and requirements.

