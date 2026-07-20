# EventGeek: List Company Contacts

Retrieves company contact records from EventGeek.

```
GET https://connect.mindcloud.co/v1/universal/eventGeek/latest/actions/list-company-contacts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a EventGeek `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/eventGeek/latest/actions/list-company-contacts?connectionId=$CONNECTION_ID&company_id=Q29tcGFueS0zMTU0MQ" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "company_id": "Q29tcGFueS0zMTU0MQ"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/eventGeek/latest/actions/list-company-contacts?${params}`, {
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
| `company_id` | string | yes | Circa company identifier. Default: `Q29tcGFueS0zMTU0MQ`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "company_id": "string",
      "email": "ava@example.com",
      "first_name": "Ava",
      "id": "string",
      "last_name": "Chen",
      "title": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `company_id` | string |  |
| `email` | string |  |
| `first_name` | string |  |
| `id` | string |  |
| `last_name` | string |  |
| `title` | string |  |

## Native endpoint

Through the native EventGeek API, this operation is `GET /companies/:company_id/contacts` (base URL `https://app.circa.co/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-company-contacts.md) for the provider-specific parameters and requirements.

