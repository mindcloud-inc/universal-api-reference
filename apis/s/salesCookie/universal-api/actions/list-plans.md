# Sales Cookie: List Plans

Retrieves commission plans from Sales Cookie.

```
GET https://connect.mindcloud.co/v1/universal/salesCookie/latest/actions/list-plans
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Sales Cookie `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/salesCookie/latest/actions/list-plans?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/salesCookie/latest/actions/list-plans?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "access": "string",
      "created": "2026-05-07T12:00:00.000Z",
      "createdById": "string",
      "customProperties": "string",
      "debugTransactionFilter": true,
      "debugTransactionId": "string",
      "description": "string",
      "id": "string",
      "isDeleted": true,
      "isSnapshot": true,
      "logging": "string",
      "name": "Ava Chen",
      "periodType": "string",
      "planDescriptorXml": "string",
      "prevAccess": "string",
      "status": "string",
      "tag": "string",
      "updated": "2026-05-07T12:00:00.000Z",
      "updatedById": "string",
      "version": 1,
      "viewCrediting": "string",
      "workspaceId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `access` | string |  |
| `created` | date |  |
| `createdById` | string |  |
| `customProperties` | string |  |
| `debugTransactionFilter` | boolean |  |
| `debugTransactionId` | string |  |
| `description` | string |  |
| `id` | string |  |
| `isDeleted` | boolean |  |
| `isSnapshot` | boolean |  |
| `logging` | string |  |
| `name` | string |  |
| `periodType` | string |  |
| `planDescriptorXml` | string |  |
| `prevAccess` | string |  |
| `status` | string |  |
| `tag` | string |  |
| `updated` | date |  |
| `updatedById` | string |  |
| `version` | number |  |
| `viewCrediting` | string |  |
| `workspaceId` | string |  |

## Native endpoint

Through the native Sales Cookie API, this operation is `GET /odata/:apiKey/Plan` (base URL `https://salescookie.com/app`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-plans.md) for the provider-specific parameters and requirements.

