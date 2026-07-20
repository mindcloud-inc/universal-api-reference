# Explorium: Update Prospects Enrollments

Updates prospect event enrollments in Explorium API.

```
PUT https://connect.mindcloud.co/v1/universal/exploriumAPI/latest/actions/update-prospects-enrollments
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Explorium `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/exploriumAPI/latest/actions/update-prospects-enrollments" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "enrollment_key": "string",
  "event_types[]": [
    "string"
  ],
  "prospect_ids[]": [
    "string"
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/exploriumAPI/latest/actions/update-prospects-enrollments', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "enrollment_key": "string",
    "event_types[]": ["string"],
    "prospect_ids[]": ["string"]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `enrollment_key` | string | yes | The client-defined enrollment key. |
| `event_types[]` | array<string> | yes | The prospect event types to enroll for. |
| `prospect_ids[]` | array<string> | yes | The Explorium prospect identifiers to enroll. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "responseContext": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `responseContext` | object | Raw API response context. |

## Native endpoint

Through the native Explorium API, this operation is `POST /v1/prospects/events/enrollments` (base URL `https://api.explorium.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-prospects-enrollments.md) for the provider-specific parameters and requirements.

