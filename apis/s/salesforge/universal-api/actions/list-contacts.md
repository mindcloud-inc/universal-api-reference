# Salesforge: List Contacts

Retrieves contacts from Salesforge.

```
GET https://connect.mindcloud.co/v1/universal/salesforge/latest/actions/list-contacts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Salesforge `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/salesforge/latest/actions/list-contacts?connectionId=$CONNECTION_ID&limit=25&offset=0&workspaceId=wks_lxxtq91neaixc8yaiqp7w" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "workspaceId": "wks_lxxtq91neaixc8yaiqp7w"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/salesforge/latest/actions/list-contacts?${params}`, {
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
| `workspaceId` | string | yes | Example: `wks_lxxtq91neaixc8yaiqp7w`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `tagIds[]` | array<string> | no | Example: `tag_123`. |
| `notInSequenceId` | string | no | Example: `seq_123`. |
| `validationStatuses[]` | array<string> | no | Example: `valid`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "company": "string",
      "customVars": {},
      "email": "ava@example.com",
      "firstName": "Ava",
      "id": "string",
      "lastName": "Chen",
      "linkedinUrl": "https://example.com",
      "tags": [
        "string"
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `company` | string |  |
| `customVars` | object |  |
| `email` | string |  |
| `firstName` | string |  |
| `id` | string |  |
| `lastName` | string |  |
| `linkedinUrl` | string |  |
| `tags` | array<string> |  |

## Native endpoint

Through the native Salesforge API, this operation is `GET /public/v2/workspaces/:workspaceID/contacts` (base URL `https://api.salesforge.ai`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-contacts.md) for the provider-specific parameters and requirements.

