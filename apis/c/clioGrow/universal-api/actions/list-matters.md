# Clio Grow: List Matters



```
GET https://connect.mindcloud.co/v1/universal/clioGrow/latest/actions/list-matters
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Clio Grow `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/clioGrow/latest/actions/list-matters?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/clioGrow/latest/actions/list-matters?${params}`, {
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

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `createdSince` | date | no | Only include matters created on or after this ISO-8601 timestamp. |
| `updatedSince` | date | no | Only include matters updated on or after this ISO-8601 timestamp. |
| `inboxLeadId` | string | no | Only include matters associated with this inbox lead ID. |
| `submittedOnly` | boolean | no | Only include submitted matters when true. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "client": {},
      "clioId": 1,
      "createdAt": "2026-05-07T12:00:00.000Z",
      "description": "string",
      "globalId": "string",
      "hiredDate": "2026-05-07T12:00:00.000Z",
      "id": 1,
      "inboxLeadId": 1,
      "isLocked": true,
      "location": "string",
      "primaryContact": {},
      "projectedValue": 1,
      "status": "string",
      "statusCategory": "string",
      "type": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `client` | object |  |
| `clioId` | number |  |
| `createdAt` | date |  |
| `description` | string |  |
| `globalId` | string |  |
| `hiredDate` | date |  |
| `id` | number |  |
| `inboxLeadId` | number |  |
| `isLocked` | boolean |  |
| `location` | string |  |
| `primaryContact` | object |  |
| `projectedValue` | number |  |
| `status` | string |  |
| `statusCategory` | string |  |
| `type` | string |  |
| `updatedAt` | date |  |

## Native endpoint

Through the native Clio Grow API, this operation is `GET /matters` (base URL `https://api.clio.com/grow`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-matters.md) for the provider-specific parameters and requirements.

