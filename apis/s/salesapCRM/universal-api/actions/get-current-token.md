# SalesapCRM: Get Current Token

Retrieves the current token details from SalesapCRM.

```
GET https://connect.mindcloud.co/v1/universal/salesapCRM/latest/actions/get-current-token
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SalesapCRM `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/salesapCRM/latest/actions/get-current-token?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/salesapCRM/latest/actions/get-current-token?${params}`, {
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
      "attributes": {
        "created-at": "2026-05-07T12:00:00.000Z",
        "options": {},
        "scopes": [
          "string"
        ],
        "token": "string",
        "updated-at": "2026-05-07T12:00:00.000Z",
        "user-id": 1
      },
      "id": "string",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `attributes.created-at` | date | Creation timestamp. |
| `attributes.options` | object | Marketplace application options associated with the token. |
| `attributes.scopes` | array<string> | Scopes associated with the token. |
| `attributes.token` | string | API token value returned by SalesapCRM; treated as sensitive. |
| `attributes.updated-at` | date | Update timestamp. |
| `attributes.user-id` | number | SalesapCRM user ID that owns the token. |
| `id` | string | Token record ID. |
| `type` | string | JSON API resource type. |

## Native endpoint

Through the native SalesapCRM API, this operation is `GET /current-token` (base URL `https://app.salesap.ru/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-current-token.md) for the provider-specific parameters and requirements.

