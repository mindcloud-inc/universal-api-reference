# Coast: Update Location By ID



```
PUT https://connect.mindcloud.co/v1/universal/coast/latest/actions/updatelocation
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Coast `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/coast/latest/actions/updatelocation" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "locationId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/coast/latest/actions/updatelocation', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "locationId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `locationId` | string | yes | Coast location ID of the location to update. |
| `name` | string | no | Updated name for the location. |
| `streetAddress` | string | no | Updated street address for the location. |
| `streetAddress2` | string | no | Updated second street-address line for the location. |
| `city` | string | no | Updated city for the location. |
| `state` | string | no | Updated state for the location. |
| `zip` | string | no | Updated ZIP code for the location. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Coast API returns.

## Native endpoint

Through the native Coast API, this operation is `PATCH /v2/locations/:locationId` (base URL `https://public.coastpay.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/updatelocation.md) for the provider-specific parameters and requirements.

