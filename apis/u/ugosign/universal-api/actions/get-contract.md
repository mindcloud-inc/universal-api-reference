# Ugosign: Get Contract

Retrieves a contract from Ugosign.

```
GET https://connect.mindcloud.co/v1/universal/ugosign/latest/actions/get-contract
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Ugosign `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ugosign/latest/actions/get-contract?connectionId=$CONNECTION_ID&contract=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "contract": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/ugosign/latest/actions/get-contract?${params}`, {
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
| `contract` | string | yes |  |

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
      "customVars": [
        {
          "description": "string",
          "id": "string",
          "slug": "string",
          "title": "string",
          "type": "string"
        }
      ],
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
| `customVars[].description` | string |  |
| `customVars[].id` | string |  |
| `customVars[].slug` | string |  |
| `customVars[].title` | string |  |
| `customVars[].type` | string |  |
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

Through the native Ugosign API, this operation is `GET /v1/contracts/:contract` (base URL `https://app.ugosign.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-contract.md) for the provider-specific parameters and requirements.

