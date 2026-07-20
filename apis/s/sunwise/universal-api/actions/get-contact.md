# Sunwise: Get Contact

Retrieves a contact from Sunwise.

```
GET https://connect.mindcloud.co/v1/universal/sunwise/latest/actions/get-contact
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Sunwise `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sunwise/latest/actions/get-contact?connectionId=$CONNECTION_ID&contact_id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "contact_id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sunwise/latest/actions/get-contact?${params}`, {
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
| `contact_id` | string | yes | Sunwise contact identifier |

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

Through the native Sunwise API, this operation is `GET /contacts/:contact_id/` (base URL `https://production.sunwise.ai/boty/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-contact.md) for the provider-specific parameters and requirements.

