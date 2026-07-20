# Crexendo: Count Domains

Retrieves a domain count from Crexendo.

```
GET https://connect.mindcloud.co/v1/universal/crexendo/latest/actions/count-domains
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Crexendo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/crexendo/latest/actions/count-domains?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/crexendo/latest/actions/count-domains?${params}`, {
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
      "total": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `total` | number |  |

## Native endpoint

Through the native Crexendo API, this operation is `GET /domains/count` (base URL `https://ns-api.com/ns-api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/count-domains.md) for the provider-specific parameters and requirements.

