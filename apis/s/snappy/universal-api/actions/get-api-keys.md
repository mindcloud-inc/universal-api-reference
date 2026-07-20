# Snappy: Get API Keys

Retrieves API keys from Snappy.

```
GET https://connect.mindcloud.co/v1/universal/snappy/latest/actions/get-api-keys
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Snappy `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/snappy/latest/actions/get-api-keys?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/snappy/latest/actions/get-api-keys?${params}`, {
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
      "accountsAccess": {
        "ids": [
          "string"
        ],
        "scope": "string"
      },
      "companyId": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "enforceMtls": true,
      "expirationDate": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "name": "Ava Chen",
      "permissions": [
        "string"
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accountsAccess.ids` | array<string> | Account IDs included in the API key scope when Snappy limits access. |
| `accountsAccess.scope` | string | Account access scope for the API key. |
| `companyId` | string | Snappy company identifier for the API key. |
| `createdAt` | date | Creation timestamp for the API key. |
| `enforceMtls` | boolean | Whether mTLS is enforced for the API key. |
| `expirationDate` | date | Expiration date for the API key when present. |
| `id` | string | Snappy API key identifier. |
| `name` | string | Name of the API key. |
| `permissions` | array<string> | Permissions granted to the API key. |

## Native endpoint

Through the native Snappy API, this operation is `GET /authentication/apiKeys` (base URL `https://api.snappy.com/public-api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-api-keys.md) for the provider-specific parameters and requirements.

