# Documo: List API Keys

Retrieves API key records from Documo.

```
GET https://connect.mindcloud.co/v1/universal/documo/latest/actions/list-api-keys
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Documo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/documo/latest/actions/list-api-keys?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/documo/latest/actions/list-api-keys?${params}`, {
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
| `userId` | string | no | User UUID to filter API keys by owner. |
| `accountId` | string | no | Account UUID to filter API keys. |
| `search` | string | no | Keyword to search in the API key name. |
| `limit` | number | no | Number of results per page. Default 20, max 100. |
| `page` | number | no | Results page number. Default 1. |
| `status` | string | no | Filter API keys by status. Possible values: active, expired. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "count": 1,
      "rows": [
        {
          "account": {
            "accountName": "Ava Chen"
          },
          "accountId": "string",
          "createdAt": "2026-05-07T12:00:00.000Z",
          "expiresAt": "2026-05-07T12:00:00.000Z",
          "id": "string",
          "name": "Ava Chen",
          "user": {
            "email": "ava@example.com"
          },
          "userId": "string"
        }
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `count` | number |  |
| `rows[].account.accountName` | string |  |
| `rows[].accountId` | string |  |
| `rows[].createdAt` | date |  |
| `rows[].expiresAt` | date |  |
| `rows[].id` | string |  |
| `rows[].name` | string |  |
| `rows[].user.email` | string |  |
| `rows[].userId` | string |  |

## Native endpoint

Through the native Documo API, this operation is `GET /api-keys` (base URL `https://api.documo.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-api-keys.md) for the provider-specific parameters and requirements.

