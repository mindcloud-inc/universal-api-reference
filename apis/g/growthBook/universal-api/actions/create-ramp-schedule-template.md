# GrowthBook: Create a single rampScheduleTemplate

Creates a new ramp schedule template in GrowthBook.

```
POST https://connect.mindcloud.co/v1/universal/growthBook/latest/actions/create-ramp-schedule-template
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GrowthBook `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/growthBook/latest/actions/create-ramp-schedule-template" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "sample",
  "steps[]": [
    "sample"
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/growthBook/latest/actions/create-ramp-schedule-template', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "sample",
    "steps[]": ["sample"]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | yes | Default: `sample`. |
| `steps[]` | array<object> | yes | Default: `["sample"]`. |
| `endPatch` | object | no |  |
| `official` | boolean | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "rampScheduleTemplate": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `rampScheduleTemplate` | object |  |

## Native endpoint

Through the native GrowthBook API, this operation is `POST /ramp-schedule-templates` (base URL `https://api.growthbook.io/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-ramp-schedule-template.md) for the provider-specific parameters and requirements.

