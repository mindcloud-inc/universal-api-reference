# Snappy: Expire Gift

Expires an existing unclaimed gift in Snappy.

```
PUT https://connect.mindcloud.co/v1/universal/snappy/latest/actions/expire-gift
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Snappy `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/snappy/latest/actions/expire-gift" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "companyId": "string",
  "giftId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/snappy/latest/actions/expire-gift', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "companyId": "string",
    "giftId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `companyId` | string | yes |  |
| `giftId` | string | yes |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Snappy API returns.

## Native endpoint

Through the native Snappy API, this operation is `POST /gifts/{giftId}/expire` (base URL `https://api.snappy.com/public-api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/expire-gift.md) for the provider-specific parameters and requirements.

