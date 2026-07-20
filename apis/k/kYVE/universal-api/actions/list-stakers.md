# KYVE: List Stakers



```
GET https://connect.mindcloud.co/v1/universal/kYVE/latest/actions/list-stakers
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a KYVE `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/kYVE/latest/actions/list-stakers?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/kYVE/latest/actions/list-stakers?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `status` | string | no | Optional staker status filter. |
| `search` | string | no | Optional staker moniker or address search. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "pagination": {},
      "stakers": [
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
| `pagination` | object |  |
| `stakers` | array<object> |  |

## Native endpoint

Through the native KYVE API, this operation is `GET /kyve/query/v1/stakers` (base URL `https://api.kyve.network`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-stakers.md) for the provider-specific parameters and requirements.

