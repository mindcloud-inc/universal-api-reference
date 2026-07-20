# OkoCRM: Get company

Retrieves company details from OkoCRM.

```
GET https://connect.mindcloud.co/v1/universal/okoCRM/latest/actions/get-company
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a OkoCRM `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/okoCRM/latest/actions/get-company?connectionId=$CONNECTION_ID&company_id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "company_id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/okoCRM/latest/actions/get-company?${params}`, {
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
| `company_id` | number | yes | The OkoCRM company ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "created_at": "2026-05-07T12:00:00.000Z",
      "emails": [
        {}
      ],
      "full_name": "Ava Chen",
      "id": 1,
      "name": "Ava Chen",
      "phones": [
        {}
      ],
      "tabs": [
        {}
      ],
      "tags": [
        {}
      ],
      "updated_at": "2026-05-07T12:00:00.000Z",
      "user_id": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `created_at` | date |  |
| `emails` | array<object> |  |
| `full_name` | string |  |
| `id` | number |  |
| `name` | string |  |
| `phones` | array<object> |  |
| `tabs` | array<object> |  |
| `tags` | array<object> |  |
| `updated_at` | date |  |
| `user_id` | number |  |

## Native endpoint

Through the native OkoCRM API, this operation is `GET /companies/[:company_id]/` (base URL `https://api.okocrm.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-company.md) for the provider-specific parameters and requirements.

