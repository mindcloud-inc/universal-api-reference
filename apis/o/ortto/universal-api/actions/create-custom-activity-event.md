# Ortto: Create Custom Activity Event



```
POST https://connect.mindcloud.co/v1/universal/ortto/latest/actions/create-custom-activity-event
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Ortto `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/ortto/latest/actions/create-custom-activity-event" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "activities[]": [
    {}
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/ortto/latest/actions/create-custom-activity-event', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "activities[]": [{}]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `activities[]` | array<object> | yes | Array of activity events to create. |
| `merge_by[]` | array<string> | no | Person field IDs used to find or create the associated person. |
| `async` | boolean | no | Queue the activity event asynchronously. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "activities": [
        {
          "personStatus": "string",
          "status": "string"
        }
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `activities[].personStatus` | string |  |
| `activities[].status` | string |  |

## Native endpoint

Through the native Ortto API, this operation is `POST /activities/create` (base URL `{{credentials.apiBaseUrl}}/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-custom-activity-event.md) for the provider-specific parameters and requirements.

