# Retently: Send Transactional Survey

Sends a transactional survey through Retently.

```
POST https://connect.mindcloud.co/v1/universal/retently/latest/actions/send-transactional-survey
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Retently `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/retently/latest/actions/send-transactional-survey" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "campaign": "string",
  "subscribers[]": [
    "string"
  ],
  "subscribers[].email": "ava@example.com",
  "subscribers[].properties[].label": "string",
  "subscribers[].properties[].type": "string",
  "subscribers[].properties[].value": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/retently/latest/actions/send-transactional-survey', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "campaign": "string",
    "subscribers[]": ["string"],
    "subscribers[].email": "ava@example.com",
    "subscribers[].properties[].label": "string",
    "subscribers[].properties[].type": "string",
    "subscribers[].properties[].value": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `campaign` | string | yes | The campaign ID where your customers will be surveyed |
| `delay` | number | no | Send the survey at a later day from the triggered event. The delay is counted in days (e.g., âdelayâ: 7); |
| `subscribers[]` | array<string> | yes | An array of objects that may contain 1 or up to 100 customers per request. Each customer object may include the following parameters: |
| `subscribers[].email` | string | yes | A variable with the email address of the customer |
| `subscribers[].firstName` | string | no | A variable with the first name of the customer |
| `subscribers[].lastName` | string | no | A variable with the last name of the customer |
| `subscribers[].company` | string | no | A variable with the company name of the customer |
| `subscribers[].tags[]` | array<string> | no | Any data passed in the array, will be imported as tags along with the customer. Example: [âfooâ, âbarâ, âbazâ] |
| `subscribers[].properties[]` | array<object> | no | Customer properties to send with the transactional survey. |
| `subscribers[].properties[].label` | string | yes | Property label |
| `subscribers[].properties[].type` | string | yes | Property type |
| `subscribers[].properties[].value` | string | yes | Property value |

## Response

```json
{
  "success": true,
  "data": [
    {
      "code": 1,
      "message": "string",
      "status": "string",
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `code` | number |  |
| `message` | string |  |
| `status` | string |  |
| `success` | boolean |  |

## Native endpoint

Through the native Retently API, this operation is `POST /api/v2/survey` (base URL `https://app.retently.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/send-transactional-survey.md) for the provider-specific parameters and requirements.

