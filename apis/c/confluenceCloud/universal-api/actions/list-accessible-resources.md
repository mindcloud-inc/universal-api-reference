# Confluence: List Accessible Resources

Retrieves accessible Confluence sites for an OAuth app.

```
GET https://connect.mindcloud.co/v1/universal/confluenceCloud/latest/actions/list-accessible-resources
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Confluence `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/confluenceCloud/latest/actions/list-accessible-resources?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/confluenceCloud/latest/actions/list-accessible-resources?${params}`, {
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
| `avatarUrl` | string | Avatar URL for the site, when available. |
| `id` | string | Cloud ID for the accessible Atlassian site. |
| `name` | string | Display name of the accessible site. |
| `scopes` | array<string> | Granted OAuth scopes for this site. |
| `url` | string | Base URL of the accessible Atlassian site. |

## Native endpoint

Through the native Confluence API, this operation is `GET /oauth/token/accessible-resources` (base URL `https://api.atlassian.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-accessible-resources.md) for the provider-specific parameters and requirements.

