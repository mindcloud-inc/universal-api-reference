# Planday: Create Absence Request

Creates a new absence request in Planday.

```
POST https://connect.mindcloud.co/v1/universal/planday/latest/actions/create-absence-request
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Planday `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/planday/latest/actions/create-absence-request" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "absencePeriod": {},
  "registrations[]": [
    {}
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/planday/latest/actions/create-absence-request', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "absencePeriod": {},
    "registrations[]": [{}]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `absencePeriod` | object | yes |  |
| `absenceType` | string | no |  |
| `note` | string | no |  |
| `registrations[]` | array<object> | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": 1,
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | number |  |
| `status` | string |  |

## Native endpoint

Through the native Planday API, this operation is `POST /absence/v1.0/absencerequests` (base URL `https://openapi.planday.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-absence-request.md) for the provider-specific parameters and requirements.

