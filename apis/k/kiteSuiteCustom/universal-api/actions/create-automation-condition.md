# Kite Suite: Create automation condition



```
POST https://connect.mindcloud.co/v1/universal/kiteSuiteCustom/latest/actions/create-automation-condition
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Kite Suite `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/kiteSuiteCustom/latest/actions/create-automation-condition" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/kiteSuiteCustom/latest/actions/create-automation-condition', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `workspace` | string | no |  |
| `createdBy` | string | no |  |
| `eventType` | string | no |  |
| `trigger` | object | no |  |
| `events[]` | array | no |  |
| `actions[]` | array | no |  |
| `description` | string | no |  |
| `isActive` | boolean | no |  |
| `isTrashed` | boolean | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "actions": [
        "string"
      ],
      "createdBy": "string",
      "description": "string",
      "events": [
        "string"
      ],
      "eventType": "string",
      "isActive": true,
      "isTrashed": true,
      "trigger": {},
      "workspace": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `actions` | array |  |
| `createdBy` | string | The ID of the user who created the automation |
| `description` | string |  |
| `events` | array |  |
| `eventType` | string | The type of event |
| `isActive` | boolean |  |
| `isTrashed` | boolean |  |
| `trigger` | object |  |
| `workspace` | string | The ID of the workspace |

## Native endpoint

Through the native Kite Suite API, this operation is `POST /api/v1/automation` (base URL `https://api.kitesuite.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-automation-condition.md) for the provider-specific parameters and requirements.

