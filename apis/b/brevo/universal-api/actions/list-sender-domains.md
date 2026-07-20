# Brevo: List Sender Domains



```
GET https://connect.mindcloud.co/v1/universal/brevo/latest/actions/list-sender-domains
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Brevo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/brevo/latest/actions/list-sender-domains?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/brevo/latest/actions/list-sender-domains?${params}`, {
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
      "count": 1,
      "current_page": 1,
      "domains": [
        {}
      ],
      "total_pages": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `count` | number | The number of domains. |
| `current_page` | number | The current page. |
| `domains` | array<object> | The sender domains. |
| `total_pages` | number | The total pages. |

## Native endpoint

Through the native Brevo API, this operation is `GET /v3/senders/domains` (base URL `https://api.brevo.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-sender-domains.md) for the provider-specific parameters and requirements.

