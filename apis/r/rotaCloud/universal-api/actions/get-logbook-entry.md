# RotaCloud: Get Logbook Entry



```
GET https://connect.mindcloud.co/v1/universal/rotaCloud/latest/actions/get-logbook-entry
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a RotaCloud `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/rotaCloud/latest/actions/get-logbook-entry?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/rotaCloud/latest/actions/get-logbook-entry?${params}`, {
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
      "categoryId": 1,
      "createdAt": "string",
      "createdBy": 1,
      "date": "string",
      "description": "string",
      "id": 1,
      "name": "Ava Chen",
      "time": "string",
      "updatedAt": "string",
      "updatedBy": 1,
      "userId": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `categoryId` | number |  |
| `createdAt` | string |  |
| `createdBy` | number |  |
| `date` | string |  |
| `description` | string |  |
| `id` | number |  |
| `name` | string |  |
| `time` | string |  |
| `updatedAt` | string |  |
| `updatedBy` | number |  |
| `userId` | number |  |

## Native endpoint

Through the native RotaCloud API, this operation is `GET /v2/logbook/:id` (base URL `https://api.rotacloud.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-logbook-entry.md) for the provider-specific parameters and requirements.

