# ActiveCampaign: List Deals

Retrieves deals from ActiveCampaign.

```
GET https://connect.mindcloud.co/v1/universal/activeCampaign/latest/actions/list-deals
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ActiveCampaign `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [filtering](../filtering.md) (`where`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/activeCampaign/latest/actions/list-deals?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/activeCampaign/latest/actions/list-deals?${params}`, {
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
      "deals": [
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
| `deals` | array<object> |  |
| `meta` | object |  |

## Native endpoint

Through the native ActiveCampaign API, this operation is `GET /deals` (base URL `{{credentials.apiUrl}}/api/3`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-deals.md) for the provider-specific parameters and requirements.

