# Tremendous: List Funding Sources

Retrieves funding sources from Tremendous.

```
GET https://connect.mindcloud.co/v1/universal/tremendous/latest/actions/list-funding-sources
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Tremendous `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/tremendous/latest/actions/list-funding-sources?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/tremendous/latest/actions/list-funding-sources?${params}`, {
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
      "funding_sources": [
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
| `funding_sources` | array<object> |  |

## Native endpoint

Through the native Tremendous API, this operation is `GET /funding_sources` (base URL `https://testflight.tremendous.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-funding-sources.md) for the provider-specific parameters and requirements.

