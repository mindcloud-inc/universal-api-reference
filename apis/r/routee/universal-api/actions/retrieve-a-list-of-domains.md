# Routee: Retrieve a list of domains

Retrieves a list of domains from Routee.

```
GET https://connect.mindcloud.co/v1/universal/routee/latest/actions/retrieve-a-list-of-domains
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Routee `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/routee/latest/actions/retrieve-a-list-of-domains?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/routee/latest/actions/retrieve-a-list-of-domains?${params}`, {
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
      "accountId": "string",
      "dkimKey": "string",
      "name": "Ava Chen",
      "selector": "string",
      "senders": [
        [
          {}
        ]
      ],
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accountId` | string |  |
| `dkimKey` | string |  |
| `name` | string |  |
| `selector` | string |  |
| `senders[]` | array<object> |  |
| `senders[].name` | string |  |
| `senders[].status` | string |  |
| `status` | string |  |

## Native endpoint

Through the native Routee API, this operation is `GET /email-senders/domain` (base URL `https://connect.routee.net`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-a-list-of-domains.md) for the provider-specific parameters and requirements.

