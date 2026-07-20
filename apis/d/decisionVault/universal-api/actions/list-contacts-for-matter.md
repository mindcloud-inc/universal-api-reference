# DecisionVault: List Contacts for Matter

Retrieves contacts for a matter in DecisionVault.

```
GET https://connect.mindcloud.co/v1/universal/decisionVault/latest/actions/list-contacts-for-matter
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DecisionVault `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/decisionVault/latest/actions/list-contacts-for-matter?connectionId=$CONNECTION_ID&matterId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "matterId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/decisionVault/latest/actions/list-contacts-for-matter?${params}`, {
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
| `matterId` | string | yes | The matter ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "addresses": [
        {}
      ],
      "also_known_as": "string",
      "created_at": "2026-05-07T12:00:00.000Z",
      "date_of_birth": "2026-05-07T12:00:00.000Z",
      "date_of_death": "2026-05-07T12:00:00.000Z",
      "email_addresses": [
        {}
      ],
      "first_name": "Ava",
      "for_matter": "string",
      "full_name": "Ava Chen",
      "gender_binary": "string",
      "id": "string",
      "is_client": true,
      "last_name": "Chen",
      "middle_name": "Ava Chen",
      "phone_numbers": [
        {}
      ],
      "preferred_name": "Ava Chen",
      "relationship": {},
      "suffix": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `addresses` | array<object> |  |
| `also_known_as` | string |  |
| `created_at` | date |  |
| `date_of_birth` | date |  |
| `date_of_death` | date |  |
| `email_addresses` | array<object> |  |
| `first_name` | string |  |
| `for_matter` | string |  |
| `full_name` | string |  |
| `gender_binary` | string |  |
| `id` | string |  |
| `is_client` | boolean |  |
| `last_name` | string |  |
| `middle_name` | string |  |
| `phone_numbers` | array<object> |  |
| `preferred_name` | string |  |
| `relationship` | object |  |
| `suffix` | string |  |

## Native endpoint

Through the native DecisionVault API, this operation is `GET /matters/:matter_id/contacts` (base URL `https://api.decisionvault.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-contacts-for-matter.md) for the provider-specific parameters and requirements.

