# Frontegg: Get Domain Restrictions

Retrieves domain restrictions for a Frontegg account.

```
GET https://connect.mindcloud.co/v1/universal/frontegg/latest/actions/get-domain-restrictions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Frontegg `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/frontegg/latest/actions/get-domain-restrictions?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/frontegg/latest/actions/get-domain-restrictions?${params}`, {
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
      "_links": {},
      "_metadata": {},
      "items": [
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
| `_links` | object |  |
| `_metadata` | object |  |
| `items` | array<object> |  |

## Native endpoint

Through the native Frontegg API, this operation is `GET /identity/resources/configurations/restrictions/v1/email-domain` (base URL `https://api.frontegg.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-domain-restrictions.md) for the provider-specific parameters and requirements.

