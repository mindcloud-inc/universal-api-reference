# AntsRoute: Update Order by External ID

Updates an existing order in AntsRoute by external ID.

```
PUT https://connect.mindcloud.co/v1/universal/antsRoute/latest/actions/update-order-by-external-id
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a AntsRoute `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/antsRoute/latest/actions/update-order-by-external-id" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "externalId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/antsRoute/latest/actions/update-order-by-external-id', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "externalId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `comments` | string | no | Order comments. |
| `externalId` | string | yes | External order ID. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native AntsRoute API returns.

## Native endpoint

Through the native AntsRoute API, this operation is `PATCH /capi/order/external-id/:externalId` (base URL `https://app.antsroute.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-order-by-external-id.md) for the provider-specific parameters and requirements.

