# Livestorm: Bulk Register Session People

Registers multiple people for a session in Livestorm.

```
POST https://connect.mindcloud.co/v1/universal/livestorm/latest/actions/bulk-register-session-people
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Livestorm `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/livestorm/latest/actions/bulk-register-session-people" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/livestorm/latest/actions/bulk-register-session-people', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes | Session ID |
| `data.attributes.tasks[]` | array<object> | no |  |
| `data.attributes.tasks[].fields[]` | array<object> | no |  |
| `data.attributes.tasks[].fields[].id` | string | no |  |
| `data.attributes.tasks[].fields[].value` | string | no |  |
| `data.attributes.tasks[].referrer` | string | no |  |
| `data.attributes.tasks[].utmSource` | string | no |  |
| `data.attributes.tasks[].utmMedium` | string | no |  |
| `data.attributes.tasks[].utmTerm` | string | no |  |
| `data.attributes.tasks[].utmContent` | string | no |  |
| `data.attributes.tasks[].utmCampaign` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "attributes": {
        "avatarLink": "https://example.com",
        "input": [
          [
            {}
          ]
        ],
        "organizationId": "string",
        "source": "string",
        "status": "string",
        "totalFail": 1,
        "totalProcessedTasks": 1,
        "totalSuccess": 1,
        "totalTasks": 1
      },
      "id": "string",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `attributes.avatarLink` | string |  |
| `attributes.input[]` | array<object> |  |
| `attributes.input[].fields[]` | array<object> |  |
| `attributes.input[].fields[].id` | string |  |
| `attributes.input[].fields[].value` | string |  |
| `attributes.input[].referrer` | string |  |
| `attributes.input[].utmCampaign` | string |  |
| `attributes.input[].utmContent` | string |  |
| `attributes.input[].utmMedium` | string |  |
| `attributes.input[].utmSource` | string |  |
| `attributes.input[].utmTerm` | string |  |
| `attributes.organizationId` | string |  |
| `attributes.source` | string |  |
| `attributes.status` | string |  |
| `attributes.totalFail` | number |  |
| `attributes.totalProcessedTasks` | number |  |
| `attributes.totalSuccess` | number |  |
| `attributes.totalTasks` | number |  |
| `id` | string | ID |
| `type` | string | Type |

## Native endpoint

Through the native Livestorm API, this operation is `POST sessions/:id/people/bulk` (base URL `https://api.livestorm.co/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/bulk-register-session-people.md) for the provider-specific parameters and requirements.

