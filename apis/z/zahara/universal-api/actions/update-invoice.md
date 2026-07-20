# Zahara: Update Invoice

Updates an existing invoice in Zahara.

```
PUT https://connect.mindcloud.co/v1/universal/zahara/latest/actions/update-invoice
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zahara `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/zahara/latest/actions/update-invoice" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "documentId": "30670"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/zahara/latest/actions/update-invoice', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "documentId": "30670"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `documentId` | number | yes | Invoice document ID to update. Example: `30670`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "DocumentId": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `DocumentId` | number | Invoice document ID represented for update operations in MindCloud. |

## Native endpoint

Through the native Zahara API, this operation is `PUT /api/{{credentials.businessUnitApiKey}}/Invoice/Update/{{documentId}}` (base URL `https://api.myzahara.net`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-invoice.md) for the provider-specific parameters and requirements.

