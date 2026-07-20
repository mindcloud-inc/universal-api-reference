# SynergyCRM: List Deal Stage Categories



```
GET https://connect.mindcloud.co/v1/universal/synergyCRM/latest/actions/list-deal-stage-categories
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SynergyCRM `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/synergyCRM/latest/actions/list-deal-stage-categories?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/synergyCRM/latest/actions/list-deal-stage-categories?${params}`, {
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
      "attributes": {},
      "id": "string",
      "links": {},
      "relationships": {},
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `attributes` | object |  |
| `id` | string |  |
| `links` | object |  |
| `relationships` | object |  |
| `type` | string |  |

## Native endpoint

Through the native SynergyCRM API, this operation is `GET /deal-stage-categories` (base URL `https://app.synergycrm.ru/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-deal-stage-categories.md) for the provider-specific parameters and requirements.

