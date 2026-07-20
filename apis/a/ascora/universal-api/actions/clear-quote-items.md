# Ascora: Clear Quote Items

Clears items from a quote in Ascora.

```
PUT https://connect.mindcloud.co/v1/universal/ascora/latest/actions/clear-quote-items
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Ascora `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/ascora/latest/actions/clear-quote-items" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/ascora/latest/actions/clear-quote-items', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `quoteNumber` | string | no |  |
| `removeSupplies` | boolean | no |  |
| `removeKits` | boolean | no |  |
| `removeLabour` | boolean | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `success` | boolean | Whether Ascora cleared the selected quote items. |

## Native endpoint

Through the native Ascora API, this operation is `POST /Quotes/ClearQuoteItems` (base URL `https://api.ascora.com.au`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/clear-quote-items.md) for the provider-specific parameters and requirements.

