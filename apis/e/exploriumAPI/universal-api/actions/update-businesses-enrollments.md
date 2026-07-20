# Explorium: Update Businesses Enrollments

Updates business event enrollments in Explorium API.

```
PUT https://connect.mindcloud.co/v1/universal/exploriumAPI/latest/actions/update-businesses-enrollments
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Explorium `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/exploriumAPI/latest/actions/update-businesses-enrollments" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "business_ids[]": [
    "string"
  ],
  "enrollment_key": "string",
  "event_types[]": [
    "string"
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/exploriumAPI/latest/actions/update-businesses-enrollments', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "business_ids[]": ["string"],
    "enrollment_key": "string",
    "event_types[]": ["string"]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `business_ids[]` | array<string> | yes | The Explorium business identifiers to enroll. |
| `enrollment_key` | string | yes | The client-defined enrollment key. |
| `event_types[]` | array<string> | yes | The business event types to enroll for. |

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
| `responseContext` | object | Explorium response metadata. |

## Native endpoint

Through the native Explorium API, this operation is `POST /v1/businesses/events/enrollments` (base URL `https://api.explorium.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-businesses-enrollments.md) for the provider-specific parameters and requirements.

