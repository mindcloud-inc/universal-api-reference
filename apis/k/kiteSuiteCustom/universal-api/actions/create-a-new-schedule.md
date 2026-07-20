# Kite Suite: Create a new schedule



```
POST https://connect.mindcloud.co/v1/universal/kiteSuiteCustom/latest/actions/create-a-new-schedule
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Kite Suite `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/kiteSuiteCustom/latest/actions/create-a-new-schedule" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "body": {},
  "name": "Ava Chen",
  "campaign": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/kiteSuiteCustom/latest/actions/create-a-new-schedule', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "body": {},
    "name": "Ava Chen",
    "campaign": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `body` | object | yes | Request body |
| `name` | string | yes | The name of the schedule. |
| `campaign` | string | yes | The ID of the campaign associated with the schedule. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "_id": "string",
      "activeDays": [
        "string"
      ],
      "campaign": "string",
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `_id` | string |  |
| `activeDays` | array<string> |  |
| `campaign` | string |  |
| `name` | string |  |

## Native endpoint

Through the native Kite Suite API, this operation is `POST /api/v1/campaign/schedule` (base URL `https://api.kitesuite.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-a-new-schedule.md) for the provider-specific parameters and requirements.

