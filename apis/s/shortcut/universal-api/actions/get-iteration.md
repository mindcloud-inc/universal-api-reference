# Shortcut: Get Iteration



```
GET https://connect.mindcloud.co/v1/universal/shortcut/latest/actions/get-iteration
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Shortcut `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/shortcut/latest/actions/get-iteration?connectionId=$CONNECTION_ID&iterationPublicId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "iterationPublicId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/shortcut/latest/actions/get-iteration?${params}`, {
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
| `iterationPublicId` | number | yes | The public ID of the iteration. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "2026-05-07T12:00:00.000Z",
      "description": "string",
      "endDate": "2026-05-07T12:00:00.000Z",
      "entityType": "string",
      "id": 1,
      "name": "Ava Chen",
      "startDate": "2026-05-07T12:00:00.000Z",
      "status": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | date |  |
| `description` | string |  |
| `endDate` | date |  |
| `entityType` | string |  |
| `id` | number |  |
| `name` | string |  |
| `startDate` | date |  |
| `status` | string |  |
| `updatedAt` | date |  |

## Native endpoint

Through the native Shortcut API, this operation is `GET /iterations/:iterationPublicId` (base URL `https://api.app.shortcut.com/api/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-iteration.md) for the provider-specific parameters and requirements.

