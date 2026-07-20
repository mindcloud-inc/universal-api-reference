# Snyk: List Tenants

Retrieves tenants available to the current Snyk user.

```
GET https://connect.mindcloud.co/v1/universal/snyk/latest/actions/list-tenants
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Snyk `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/snyk/latest/actions/list-tenants?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/snyk/latest/actions/list-tenants?${params}`, {
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
      "jsonapi": {},
      "links": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | array<object> |  |
| `jsonapi` | object |  |
| `links` | object |  |

## Native endpoint

Through the native Snyk API, this operation is `GET /tenants` (base URL `https://api.snyk.io/rest`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-tenants.md) for the provider-specific parameters and requirements.

