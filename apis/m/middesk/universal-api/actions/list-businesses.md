# Middesk: List Businesses

Retrieves businesses from your Middesk account.

```
GET https://connect.mindcloud.co/v1/universal/middesk/latest/actions/list-businesses
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Middesk `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/middesk/latest/actions/list-businesses?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/middesk/latest/actions/list-businesses?${params}`, {
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
      "hasMore": true,
      "object": "string",
      "totalCount": 1,
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | array<object> | List of business records returned by Middesk. |
| `hasMore` | boolean | Whether more results are available. |
| `object` | string | Envelope type returned by Middesk. |
| `totalCount` | number | Total number of businesses available for the current account. |
| `url` | string | Canonical API URL for this list response. |

## Native endpoint

Through the native Middesk API, this operation is `GET /businesses` (base URL `https://api.middesk.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-businesses.md) for the provider-specific parameters and requirements.

