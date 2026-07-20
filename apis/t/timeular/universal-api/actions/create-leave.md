# Timeular: Create Leave

Creates a new leave request in your Timeular workspace.

```
POST https://connect.mindcloud.co/v1/universal/timeular/latest/actions/create-leave
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Timeular `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/timeular/latest/actions/create-leave" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "endDate": "string",
  "startDate": "string",
  "typeId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/timeular/latest/actions/create-leave', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "endDate": "string",
    "startDate": "string",
    "typeId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `endDate` | string | yes |  |
| `note` | string | no |  |
| `startDate` | string | yes |  |
| `typeId` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "endDate": "string",
      "id": "string",
      "note": "string",
      "startDate": "string",
      "status": "string",
      "typeId": "string",
      "user": {
        "email": "ava@example.com",
        "id": "string",
        "name": "Ava Chen"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `endDate` | string |  |
| `id` | string |  |
| `note` | string |  |
| `startDate` | string |  |
| `status` | string |  |
| `typeId` | string |  |
| `user.email` | string |  |
| `user.id` | string |  |
| `user.name` | string |  |

## Native endpoint

Through the native Timeular API, this operation is `POST /api/v4/leaves` (base URL `https://api.early.app`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-leave.md) for the provider-specific parameters and requirements.

