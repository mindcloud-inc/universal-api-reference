# Dev.to: Get Organization

Retrieves a Dev.to organization by username.

```
GET https://connect.mindcloud.co/v1/universal/devto/latest/actions/get-organization
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Dev.to `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/devto/latest/actions/get-organization?connectionId=$CONNECTION_ID&username=Ava%20Chen" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "username": "Ava Chen"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/devto/latest/actions/get-organization?${params}`, {
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
| `username` | string | yes | Organization username. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "location": "string",
      "name": "Ava Chen",
      "summary": "string",
      "tag_line": "string",
      "type_of": "string",
      "username": "Ava Chen",
      "website_url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `location` | string |  |
| `name` | string |  |
| `summary` | string |  |
| `tag_line` | string |  |
| `type_of` | string |  |
| `username` | string |  |
| `website_url` | string |  |

## Native endpoint

Through the native Dev.to API, this operation is `GET /organizations/:username` (base URL `https://dev.to/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-organization.md) for the provider-specific parameters and requirements.

