# Bexio: Issue Quote

Issues a quote in Bexio.

```
PUT https://connect.mindcloud.co/v1/universal/bexio/latest/actions/issue-quote
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Bexio `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/bexio/latest/actions/issue-quote" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "quoteId": "1"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/bexio/latest/actions/issue-quote', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "quoteId": "1"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `quoteId` | number | yes | The ID of the quote. Example: `1`. |

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
| `success` | boolean |  |

## Native endpoint

Through the native Bexio API, this operation is `POST /2.0/kb_offer/:quote_id/issue` (base URL `https://api.bexio.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/issue-quote.md) for the provider-specific parameters and requirements.

