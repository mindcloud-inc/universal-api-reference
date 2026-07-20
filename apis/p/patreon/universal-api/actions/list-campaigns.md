# Patreon: List Campaigns

Retrieves campaigns owned by the authorized user from Patreon.

```
GET https://connect.mindcloud.co/v1/universal/patreon/latest/actions/list-campaigns
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Patreon `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/patreon/latest/actions/list-campaigns?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/patreon/latest/actions/list-campaigns?${params}`, {
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
      "meta": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | array<object> | Patreon JSON:API campaign resources. |
| `meta` | object | Pagination metadata returned by Patreon. |

## Native endpoint

Through the native Patreon API, this operation is `GET /campaigns` (base URL `https://www.patreon.com/api/oauth2/v2`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-campaigns.md) for the provider-specific parameters and requirements.

