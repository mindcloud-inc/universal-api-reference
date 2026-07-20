# Giftbit: Get Link URLs

Retrieves generated reward links for a Giftbit order.

```
GET https://connect.mindcloud.co/v1/universal/giftbit/latest/actions/get-link-urls
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Giftbit `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/giftbit/latest/actions/get-link-urls?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/giftbit/latest/actions/get-link-urls?${params}`, {
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
| `id` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "directlinks": [
        {}
      ],
      "info": {},
      "limit": 1,
      "number_of_results": 1,
      "offset": 1,
      "total_count": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `directlinks` | array<object> |  |
| `info` | object |  |
| `limit` | number |  |
| `number_of_results` | number |  |
| `offset` | number |  |
| `total_count` | number |  |

## Native endpoint

Through the native Giftbit API, this operation is `GET /links/:id` (base URL `https://api-testbed.giftbit.com/papi/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-link-urls.md) for the provider-specific parameters and requirements.

