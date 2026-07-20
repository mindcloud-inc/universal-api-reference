# Sunwise: List Contacts

Retrieves contacts from Sunwise.

```
GET https://connect.mindcloud.co/v1/universal/sunwise/latest/actions/list-contacts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Sunwise `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sunwise/latest/actions/list-contacts?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sunwise/latest/actions/list-contacts?${params}`, {
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

Through the native Sunwise API, this operation is `GET /contacts/` (base URL `https://production.sunwise.ai/boty/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-contacts.md) for the provider-specific parameters and requirements.

