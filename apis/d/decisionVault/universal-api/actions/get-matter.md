# DecisionVault: Get Matter

Retrieves a matter from DecisionVault by ID.

```
GET https://connect.mindcloud.co/v1/universal/decisionVault/latest/actions/get-matter
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DecisionVault `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/decisionVault/latest/actions/get-matter?connectionId=$CONNECTION_ID&matterId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "matterId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/decisionVault/latest/actions/get-matter?${params}`, {
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
      "client_may_edit": true,
      "client_type": "string",
      "close_date": "2026-05-07T12:00:00.000Z",
      "contact_main": {},
      "contact_main_marital_status": "string",
      "contact_main_status": "string",
      "contact_representative": {},
      "contact_spouse": {},
      "id": "string",
      "is_submitted": true,
      "name": "Ava Chen",
      "number_of_children": 1,
      "number_of_contacts": 1,
      "open_date": "2026-05-07T12:00:00.000Z",
      "questionnaire": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `client_may_edit` | boolean |  |
| `client_type` | string |  |
| `close_date` | date |  |
| `contact_main` | object |  |
| `contact_main_marital_status` | string |  |
| `contact_main_status` | string |  |
| `contact_representative` | object |  |
| `contact_spouse` | object |  |
| `id` | string |  |
| `is_submitted` | boolean |  |
| `name` | string |  |
| `number_of_children` | number |  |
| `number_of_contacts` | number |  |
| `open_date` | date |  |
| `questionnaire` | object |  |

## Native endpoint

Through the native DecisionVault API, this operation is `GET /matters/:matter_id` (base URL `https://api.decisionvault.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-matter.md) for the provider-specific parameters and requirements.

