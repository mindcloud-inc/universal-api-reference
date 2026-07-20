# Ugosign: List Contracts

Retrieves contracts from Ugosign.

```
GET https://connect.mindcloud.co/v1/universal/ugosign/latest/actions/list-contracts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Ugosign `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ugosign/latest/actions/list-contracts?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/ugosign/latest/actions/list-contracts?${params}`, {
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

Through the native Ugosign API, this operation is `GET /v1/contracts` (base URL `https://app.ugosign.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-contracts.md) for the provider-specific parameters and requirements.

