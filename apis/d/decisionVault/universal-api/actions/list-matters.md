# DecisionVault: List Matters

Retrieves matters from your firm in DecisionVault.

```
GET https://connect.mindcloud.co/v1/universal/decisionVault/latest/actions/list-matters
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DecisionVault `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/decisionVault/latest/actions/list-matters?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/decisionVault/latest/actions/list-matters?${params}`, {
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
| `from` | date | no | Filter matters created from this date, inclusive. |
| `isSubmitted` | number | no | Filter matters by submit status: 1 for submitted or 0 for not submitted. |
| `questApproach` | string | no | Filter matters by questionnaire approach or type. |
| `search` | string | no | Only return matters whose name contains this search term (case-insensitive). |
| `until` | date | no | Filter matters created until this date, inclusive. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "client_type": "string",
      "close_date": "2026-05-07T12:00:00.000Z",
      "contact_main_full_name": "Ava Chen",
      "contact_main_marital_status": "string",
      "contact_main_status": "string",
      "contact_spouse_full_name": "Ava Chen",
      "id": "string",
      "is_submitted": true,
      "name": "Ava Chen",
      "open_date": "2026-05-07T12:00:00.000Z",
      "quest_approach": "string",
      "quest_internal_type": "string",
      "representative_full_name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `client_type` | string |  |
| `close_date` | date |  |
| `contact_main_full_name` | string |  |
| `contact_main_marital_status` | string |  |
| `contact_main_status` | string |  |
| `contact_spouse_full_name` | string |  |
| `id` | string |  |
| `is_submitted` | boolean |  |
| `name` | string |  |
| `open_date` | date |  |
| `quest_approach` | string |  |
| `quest_internal_type` | string |  |
| `representative_full_name` | string |  |

## Native endpoint

Through the native DecisionVault API, this operation is `GET /matters` (base URL `https://api.decisionvault.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-matters.md) for the provider-specific parameters and requirements.

