# RotaCloud: List Logbook Entries



```
GET https://connect.mindcloud.co/v1/universal/rotaCloud/latest/actions/list-logbook-entries
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a RotaCloud `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/rotaCloud/latest/actions/list-logbook-entries?connectionId=$CONNECTION_ID&userId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "userId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/rotaCloud/latest/actions/list-logbook-entries?${params}`, {
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
| `date` | string | no | Filter entries by ISO 8601 date. |
| `userId` | number | yes |  |

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

Through the native RotaCloud API, this operation is `GET /v2/logbook/user/:userId` (base URL `https://api.rotacloud.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-logbook-entries.md) for the provider-specific parameters and requirements.

