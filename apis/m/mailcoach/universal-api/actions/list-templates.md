# Mailcoach: List Templates

Retrieves all templates from Mailcoach.

```
GET https://connect.mindcloud.co/v1/universal/mailcoach/latest/actions/list-templates
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Mailcoach `connectionId` ([setup](../authentication.md)).

This action also supports [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mailcoach/latest/actions/list-templates?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/mailcoach/latest/actions/list-templates?${params}`, {
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
| `filterSearch` | string | no | Search templates by name. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "2026-05-07T12:00:00.000Z",
      "fields": [
        {}
      ],
      "html": "string",
      "name": "Ava Chen",
      "structuredHtml": {},
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "uuid": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | date |  |
| `fields` | array<object> |  |
| `html` | string |  |
| `name` | string |  |
| `structuredHtml` | object |  |
| `updatedAt` | date |  |
| `uuid` | string |  |

## Native endpoint

Through the native Mailcoach API, this operation is `GET /templates` (base URL `https://mindcloud.mailcoach.app/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-templates.md) for the provider-specific parameters and requirements.

