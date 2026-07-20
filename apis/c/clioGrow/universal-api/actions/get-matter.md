# Clio Grow: Get Matter



```
GET https://connect.mindcloud.co/v1/universal/clioGrow/latest/actions/get-matter
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Clio Grow `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/clioGrow/latest/actions/get-matter?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/clioGrow/latest/actions/get-matter?${params}`, {
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
| `id` | string | yes | The unique identifier for the matter. |

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

Through the native Clio Grow API, this operation is `GET /matters/{id}` (base URL `https://api.clio.com/grow`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-matter.md) for the provider-specific parameters and requirements.

