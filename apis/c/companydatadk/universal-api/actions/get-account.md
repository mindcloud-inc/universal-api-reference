# companydata.dk: Get Account

Retrieves API key account details from companydata.dk.

```
GET https://connect.mindcloud.co/v1/universal/companydatadk/latest/actions/get-account
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a companydata.dk `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/companydatadk/latest/actions/get-account?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/companydatadk/latest/actions/get-account?${params}`, {
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
      "createdAt": "2026-05-07T12:00:00.000Z",
      "keyPrefix": "string",
      "name": "Ava Chen",
      "permissions": [
        "string"
      ],
      "rateLimit": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | date | When the current API key was created |
| `keyPrefix` | string | Masked prefix of the current API key |
| `name` | string | Display name of the current API key |
| `permissions` | array<string> | Permissions granted to the current API key |
| `rateLimit` | object | Current per-minute and per-month rate limits |

## Native endpoint

Through the native companydata.dk API, this operation is `GET /v1/account` (base URL `https://api.companydata.dk`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-account.md) for the provider-specific parameters and requirements.

