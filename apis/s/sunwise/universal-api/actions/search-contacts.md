# Sunwise: Search Contacts

Finds contacts in Sunwise by search term.

```
GET https://connect.mindcloud.co/v1/universal/sunwise/latest/actions/search-contacts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Sunwise `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sunwise/latest/actions/search-contacts?connectionId=$CONNECTION_ID&search=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "search": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sunwise/latest/actions/search-contacts?${params}`, {
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
| `search` | string | yes | Search term for matching contacts |

## Response

```json
{
  "success": true,
  "data": [
    {
      "company_name": "Ava Chen",
      "created_at": "string",
      "emails": [
        {
          "email": "ava@example.com"
        }
      ],
      "id": "string",
      "name": "Ava Chen",
      "status_flag": "string",
      "telephones": [
        {
          "telephone": "string"
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
| `company_name` | string |  |
| `created_at` | string |  |
| `emails` | array<object> |  |
| `emails[].email` | string |  |
| `id` | string |  |
| `name` | string |  |
| `status_flag` | string |  |
| `telephones` | array<object> |  |
| `telephones[].telephone` | string |  |

## Native endpoint

Through the native Sunwise API, this operation is `GET /contacts-search/` (base URL `https://production.sunwise.ai/boty/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-contacts.md) for the provider-specific parameters and requirements.

