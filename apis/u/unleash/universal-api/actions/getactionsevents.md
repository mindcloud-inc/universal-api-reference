# Unleash: [Beta] Get Action Events For A Specific Action Set.

Retrieves action events for a specific action set from Unleash.

```
GET https://connect.mindcloud.co/v1/universal/unleash/latest/actions/getactionsevents
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Unleash `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/unleash/latest/actions/getactionsevents?connectionId=$CONNECTION_ID&projectId=string&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "projectId": "string",
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/unleash/latest/actions/getactionsevents?${params}`, {
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
| `projectId` | string | yes | Required path parameter. |
| `id` | string | yes | Required path parameter. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "2026-05-07T12:00:00.000Z",
      "description": "string",
      "id": "string",
      "message": "string",
      "name": "Ava Chen",
      "success": true,
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | date | Creation timestamp. |
| `description` | string | Resource description. |
| `id` | string | Resource identifier. |
| `message` | string | Response message. |
| `name` | string | Resource name. |
| `success` | boolean | Whether the operation succeeded. |
| `updatedAt` | date | Last update timestamp. |

## Native endpoint

Through the native Unleash API, this operation is `GET /api/admin/projects/{projectId}/actions/{id}/events` (base URL `https://us.app.getunleash.io/uspp0456`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/getactionsevents.md) for the provider-specific parameters and requirements.

