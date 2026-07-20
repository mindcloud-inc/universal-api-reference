# Oneflow: Get Contact

Retrieves contact details from Oneflow.

```
GET https://connect.mindcloud.co/v1/universal/oneflow/latest/actions/get-contact
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Oneflow `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/oneflow/latest/actions/get-contact?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/oneflow/latest/actions/get-contact?${params}`, {
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
| `id` | string | yes | The Oneflow contact ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "company_name": "Ava Chen",
      "company_registration_number": "string",
      "country_code": "string",
      "created_time": "string",
      "date_of_birth": "string",
      "email": "ava@example.com",
      "id": 1,
      "name": "Ava Chen",
      "notes": "string",
      "phone_number": "string",
      "title": "string",
      "updated_time": "string",
      "workspace_id": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `company_name` | string |  |
| `company_registration_number` | string |  |
| `country_code` | string |  |
| `created_time` | string |  |
| `date_of_birth` | string |  |
| `email` | string |  |
| `id` | number |  |
| `name` | string |  |
| `notes` | string |  |
| `phone_number` | string |  |
| `title` | string |  |
| `updated_time` | string |  |
| `workspace_id` | number |  |

## Native endpoint

Through the native Oneflow API, this operation is `GET /contacts/:id` (base URL `https://api.oneflow.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-contact.md) for the provider-specific parameters and requirements.

