# Watbot: Update List Item

Updates an existing list item in Watbot.

```
PUT https://connect.mindcloud.co/v1/universal/watbot/latest/actions/update-list-item
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Watbot `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/watbot/latest/actions/update-list-item" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "schemaId": "5dee4800c2cc5a38ec797235",
  "itemId": "5dee62e46637df57be7bc686",
  "data": "[object Object]"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/watbot/latest/actions/update-list-item', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "schemaId": "5dee4800c2cc5a38ec797235",
    "itemId": "5dee62e46637df57be7bc686",
    "data": "[object Object]"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `schemaId` | string | yes | ID of the list schema. Example: `5dee4800c2cc5a38ec797235`. |
| `itemId` | string | yes | ID of the list item. Example: `5dee62e46637df57be7bc686`. |
| `data` | object | yes | Updated list item values. Example: `[object Object]`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Watbot API returns.

## Native endpoint

Through the native Watbot API, this operation is `POST /updateListItem` (base URL `https://watbot.ru/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-list-item.md) for the provider-specific parameters and requirements.

