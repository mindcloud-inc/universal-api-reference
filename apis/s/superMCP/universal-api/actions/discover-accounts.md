# SuperMCP: Discover Accounts



```
GET https://connect.mindcloud.co/v1/universal/superMCP/latest/actions/discover-accounts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SuperMCP `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/superMCP/latest/actions/discover-accounts?connectionId=$CONNECTION_ID&dataSourceId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "dataSourceId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/superMCP/latest/actions/discover-accounts?${params}`, {
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
| `dataSourceId` | string | yes | Supermetrics data source ID, such as GAWA for Google Analytics 4 or AW for Google Ads. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `filter` | string | no | Optional case-insensitive account filter against account ID, name, or group. |
| `compress` | boolean | no | Return a compact TOON response instead of JSON when supported. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "accounts": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accounts` | array<object> | Connected accounts for the requested data source. |

## Native endpoint

Through the native SuperMCP API, this operation is `POST /mcp/accounts_discovery` (base URL `https://mcp.supermetrics.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/discover-accounts.md) for the provider-specific parameters and requirements.

