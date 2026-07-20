# Zoho Writer: List Templates

Retrieves templates from Zoho Writer.

```
GET https://connect.mindcloud.co/v1/universal/zohoWriter/latest/actions/list-templates
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoho Writer `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zohoWriter/latest/actions/list-templates?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zohoWriter/latest/actions/list-templates?${params}`, {
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
| `type` | string | no | Template scope to list: personal or organization. Default: `personal`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "templates": [
        {
          "id": "string",
          "name": "Ava Chen",
          "status": "string",
          "type": "string"
        }
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `templates` | array<object> |  |
| `templates[].id` | string |  |
| `templates[].name` | string |  |
| `templates[].status` | string |  |
| `templates[].type` | string |  |

## Native endpoint

Through the native Zoho Writer API, this operation is `GET /v1/templates` (base URL `{{credentials.accessTokenRequest.api_domain}}/writer/api`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-templates.md) for the provider-specific parameters and requirements.

