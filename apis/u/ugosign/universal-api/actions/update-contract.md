# Ugosign: Update Contract

Updates an existing contract in Ugosign.

```
PUT https://connect.mindcloud.co/v1/universal/ugosign/latest/actions/update-contract
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Ugosign `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/ugosign/latest/actions/update-contract" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "contract": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/ugosign/latest/actions/update-contract', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "contract": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `allowRefusal` | string | no |  |
| `authorId` | string | no |  |
| `content` | string | no |  |
| `contract` | string | yes |  |
| `description` | string | no |  |
| `folderId` | string | no |  |
| `footer` | string | no |  |
| `initials` | string | no |  |
| `reminder` | string | no |  |
| `title` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "allowRefusal": true,
      "authorId": "string",
      "content": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "description": "string",
      "folderId": "string",
      "footer": "string",
      "id": "string",
      "initials": true,
      "message": "string",
      "organizationId": "string",
      "reminder": 1,
      "title": "string",
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
| `allowRefusal` | boolean |  |
| `authorId` | string |  |
| `content` | string |  |
| `createdAt` | date |  |
| `description` | string |  |
| `folderId` | string |  |
| `footer` | string |  |
| `id` | string |  |
| `initials` | boolean |  |
| `message` | string |  |
| `organizationId` | string |  |
| `reminder` | number |  |
| `title` | string |  |
| `type` | string |  |
| `updatedAt` | date |  |

## Native endpoint

Through the native Ugosign API, this operation is `PATCH /v1/contracts/:contract` (base URL `https://app.ugosign.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-contract.md) for the provider-specific parameters and requirements.

