# Harvest: Delete task

Deletes an existing task from Harvest.

```
DELETE https://connect.mindcloud.co/v1/universal/harvest/latest/actions/delete-task
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Harvest `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/harvest/latest/actions/delete-task?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/harvest/latest/actions/delete-task?${params}`, {
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
| `id` | number | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "billableByDefault": true,
      "createdAt": "2026-05-07T12:00:00.000Z",
      "defaultHourlyRate": 1,
      "id": 1,
      "isActive": true,
      "isDefault": true,
      "name": "Ava Chen",
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `billableByDefault` | boolean |  |
| `createdAt` | date |  |
| `defaultHourlyRate` | number |  |
| `id` | number |  |
| `isActive` | boolean |  |
| `isDefault` | boolean |  |
| `name` | string |  |
| `updatedAt` | date |  |

## Native endpoint

Through the native Harvest API, this operation is `DELETE /v2/tasks/:id` (base URL `https://api.harvestapp.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-task.md) for the provider-specific parameters and requirements.

