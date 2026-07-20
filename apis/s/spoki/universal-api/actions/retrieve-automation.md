# Spoki: Retrieve Automation

Retrieves an automation by ID.

```
GET https://connect.mindcloud.co/v1/universal/spoki/latest/actions/retrieve-automation
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Spoki `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/spoki/latest/actions/retrieve-automation?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/spoki/latest/actions/retrieve-automation?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | number | yes | The automation ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "automationGroups": [
        {}
      ],
      "createdDatetime": "2026-05-07T12:00:00.000Z",
      "firstMessageText": "string",
      "id": 1,
      "isActive": true,
      "isFavorite": true,
      "name": "Ava Chen",
      "updatedDatetime": "2026-05-07T12:00:00.000Z",
      "updatedUser": {},
      "webhookSet": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `automationGroups` | array<object> |  |
| `createdDatetime` | date |  |
| `firstMessageText` | string |  |
| `id` | number |  |
| `isActive` | boolean |  |
| `isFavorite` | boolean |  |
| `name` | string |  |
| `updatedDatetime` | date |  |
| `updatedUser` | object |  |
| `webhookSet` | array<object> |  |

## Native endpoint

Through the native Spoki API, this operation is `GET /automations/{{id}}/` (base URL `https://api.spoki.com/api/1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-automation.md) for the provider-specific parameters and requirements.

