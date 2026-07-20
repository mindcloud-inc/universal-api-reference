# OpenRegister: Get Person

Retrieves person information from OpenRegister by person ID.

```
GET https://connect.mindcloud.co/v1/universal/openRegister/latest/actions/get-person
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a OpenRegister `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/openRegister/latest/actions/get-person?connectionId=$CONNECTION_ID&personId=person_id" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "personId": "person_id"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/openRegister/latest/actions/get-person?${params}`, {
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
| `personId` | string | yes | Unique person identifier. Example: `person_id`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "city": "string",
      "date_of_birth": "2026-05-07T12:00:00.000Z",
      "first_name": "Ava",
      "id": "string",
      "last_name": "Chen",
      "management_positions": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `city` | string | City. |
| `date_of_birth` | date | Date of birth. |
| `first_name` | string | First name. |
| `id` | string | Person ID. |
| `last_name` | string | Last name. |
| `management_positions` | array<object> | Management positions. |

## Native endpoint

Through the native OpenRegister API, this operation is `GET /v1/person/:person_id` (base URL `https://api.openregister.de`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-person.md) for the provider-specific parameters and requirements.

