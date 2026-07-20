# KlipLink: List Domains



```
GET https://connect.mindcloud.co/v1/universal/klipLink/latest/actions/list-domains
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a KlipLink `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/klipLink/latest/actions/list-domains?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/klipLink/latest/actions/list-domains?${params}`, {
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
      "domains": [
        {}
      ],
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `domains` | array<object> | Domains returned by KlipLink. |
| `success` | boolean | Whether the request succeeded. |

## Native endpoint

Through the native KlipLink API, this operation is `GET /v1/domains` (base URL `https://api.klipl.ink`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-domains.md) for the provider-specific parameters and requirements.

