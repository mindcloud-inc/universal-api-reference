# Crexendo: List Domains

Retrieves domains from Crexendo.

```
GET https://connect.mindcloud.co/v1/universal/crexendo/latest/actions/list-domains
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Crexendo `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/crexendo/latest/actions/list-domains?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/crexendo/latest/actions/list-domains?${params}`, {
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
      "count-users-configured": 1,
      "description": "string",
      "domain": "string",
      "domain-type": "string",
      "reseller": "string",
      "time-zone": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `count-users-configured` | number |  |
| `description` | string |  |
| `domain` | string |  |
| `domain-type` | string |  |
| `reseller` | string |  |
| `time-zone` | string |  |

## Native endpoint

Through the native Crexendo API, this operation is `GET /domains` (base URL `https://ns-api.com/ns-api/v2`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-domains.md) for the provider-specific parameters and requirements.

