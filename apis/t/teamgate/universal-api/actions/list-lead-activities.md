# Teamgate: List Lead Activities

Retrieves activities for a lead in Teamgate.

```
GET https://connect.mindcloud.co/v1/universal/teamgate/latest/actions/list-lead-activities
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Teamgate `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/teamgate/latest/actions/list-lead-activities?connectionId=$CONNECTION_ID&limit=25&offset=0&leadId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "leadId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/teamgate/latest/actions/list-lead-activities?${params}`, {
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
| `leadId` | string | yes | Lead ID whose activities should be listed. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "canEdit": "string",
      "canView": "string",
      "created": {},
      "id": 1,
      "isDeleted": "string",
      "leads": [
        {}
      ],
      "owner": {},
      "recipients": [
        "string"
      ],
      "sender": "string",
      "status": "string",
      "subject": "string",
      "type": "string",
      "updated": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `canEdit` | string |  |
| `canView` | string |  |
| `created` | object |  |
| `id` | number |  |
| `isDeleted` | string |  |
| `leads` | array<object> |  |
| `owner` | object |  |
| `recipients` | array<string> |  |
| `sender` | string |  |
| `status` | string |  |
| `subject` | string |  |
| `type` | string |  |
| `updated` | object |  |

## Native endpoint

Through the native Teamgate API, this operation is `GET /leads/{{leadId}}/events` (base URL `https://api.teamgate.com/v4`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-lead-activities.md) for the provider-specific parameters and requirements.

