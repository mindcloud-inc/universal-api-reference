# Kite Suite: Update a campaign by its ID



```
PUT https://connect.mindcloud.co/v1/universal/kiteSuiteCustom/latest/actions/update-a-campaign-by-its-id
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Kite Suite `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/kiteSuiteCustom/latest/actions/update-a-campaign-by-its-id" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string",
  "body": {},
  "name": "Ava Chen",
  "status": "string",
  "options": {},
  "start": "string",
  "end": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/kiteSuiteCustom/latest/actions/update-a-campaign-by-its-id', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string",
    "body": {},
    "name": "Ava Chen",
    "status": "string",
    "options": {},
    "start": "string",
    "end": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes | The ID of the campaign to update. |
| `body` | object | yes | Request body |
| `name` | string | yes | The name of the campaign. |
| `status` | string | yes | The status of the campaign (e.g., "resume", "pause"). |
| `options` | object | yes | Additional campaign options. |
| `start` | string | yes | The start date of the campaign. |
| `end` | string | yes | The end date of the campaign. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "_id": "string",
      "createdBy": "string",
      "name": "Ava Chen",
      "schedules": [
        "string"
      ],
      "sequences": [
        "string"
      ],
      "status": "string",
      "workspace": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `_id` | string | Campaign ID. |
| `createdBy` | string | Tenant ID. |
| `name` | string | Campaign name. |
| `schedules` | array<string> |  |
| `sequences` | array<string> |  |
| `status` | string | Campaign status. |
| `workspace` | string | Workspace ID. |

## Native endpoint

Through the native Kite Suite API, this operation is `PATCH /api/v1/campaign/:id` (base URL `https://api.kitesuite.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-a-campaign-by-its-id.md) for the provider-specific parameters and requirements.

