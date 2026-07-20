# Megaventory: Bulk Update Sales Quotes

Updates sales quotes in Megaventory in bulk.

```
PUT https://connect.mindcloud.co/v1/universal/megaventory/latest/actions/bulk-update-sales-quotes
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Megaventory `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/megaventory/latest/actions/bulk-update-sales-quotes" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "SalesQuotes": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/megaventory/latest/actions/bulk-update-sales-quotes', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "SalesQuotes": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `SalesQuotes` | list<object> | yes | JSON array of sales quote objects. |
| `mvInsertUpdateDeleteSourceApplication` | string | no | Source application label Megaventory should store for the change. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "ResponseStatus": {},
      "SalesQuotesResponses": [
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
| `ResponseStatus` | object |  |
| `SalesQuotesResponses` | array<object> |  |

## Native endpoint

Through the native Megaventory API, this operation is `POST /json/reply/SalesQuotesUpdate` (base URL `https://api.megaventory.com/v2017a`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/bulk-update-sales-quotes.md) for the provider-specific parameters and requirements.

