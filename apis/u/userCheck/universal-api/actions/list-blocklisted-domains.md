# UserCheck: List Blocklisted Domains

Retrieves blocklisted domain entries from UserCheck.

```
GET https://connect.mindcloud.co/v1/universal/userCheck/latest/actions/list-blocklisted-domains
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a UserCheck `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/userCheck/latest/actions/list-blocklisted-domains?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/userCheck/latest/actions/list-blocklisted-domains?${params}`, {
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
      "data": [
        {}
      ],
      "links": {},
      "meta": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | array<object> |  |
| `links` | object |  |
| `meta` | object |  |

## Native endpoint

Through the native UserCheck API, this operation is `GET /blocklist` (base URL `https://api.usercheck.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-blocklisted-domains.md) for the provider-specific parameters and requirements.

