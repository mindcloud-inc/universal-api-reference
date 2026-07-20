# Gorgias: Retrieve Account

Retrieves account details from Gorgias.

```
GET https://connect.mindcloud.co/v1/universal/gorgias/latest/actions/retrieve-account
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Gorgias `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/gorgias/latest/actions/retrieve-account?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/gorgias/latest/actions/retrieve-account?${params}`, {
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
      "created_datetime": "string",
      "current_subscription": {},
      "deactivated_datetime": "string",
      "domain": "string",
      "meta": {},
      "settings": [
        {}
      ],
      "status": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `created_datetime` | string |  |
| `current_subscription` | object |  |
| `deactivated_datetime` | string |  |
| `domain` | string |  |
| `meta` | object |  |
| `settings` | array<object> |  |
| `status` | object |  |

## Native endpoint

Through the native Gorgias API, this operation is `GET /account` (base URL `https://{{credentials.subdomain}}.gorgias.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-account.md) for the provider-specific parameters and requirements.

