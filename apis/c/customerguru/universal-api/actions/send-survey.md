# Customer.guru: Send Survey

Creates a new survey send request in Customer.guru.

```
POST https://connect.mindcloud.co/v1/universal/customerguru/latest/actions/send-survey
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Customer.guru `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/customerguru/latest/actions/send-survey" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "scheduledFor": "now",
  "customers[]": [
    {}
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/customerguru/latest/actions/send-survey', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "scheduledFor": "now",
    "customers[]": [{}]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `test` | boolean | no | When true, validate without sending emails. Default: `false`. |
| `scheduledFor` | string | yes | Use now or an ISO8601 timestamp in the future. Default: `now`. |
| `surveyId` | number | no | Optional specific survey ID. Default: `{{credentials.surveyId}}`. |
| `customers[]` | array<object> | yes | Array of customer objects with email and optional language and properties fields. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "failed_to_send": 1,
      "status": "string",
      "successfully_sent": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `failed_to_send` | number |  |
| `status` | string |  |
| `successfully_sent` | number |  |

## Native endpoint

Through the native Customer.guru API, this operation is `POST /api/v2/survey` (base URL `https://customer.guru`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/send-survey.md) for the provider-specific parameters and requirements.

