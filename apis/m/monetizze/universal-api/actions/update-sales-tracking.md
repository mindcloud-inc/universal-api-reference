# Monetizze: Update Sales Tracking

Updates sales tracking codes in Monetizze.

```
PUT https://connect.mindcloud.co/v1/universal/monetizze/latest/actions/update-sales-tracking
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Monetizze `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/monetizze/latest/actions/update-sales-tracking" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "trackingRecords": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/monetizze/latest/actions/update-sales-tracking', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "trackingRecords": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `trackingRecords` | string | yes | JSON array string with objects like [{"codLog":1,"transaction":1,"trackingCode":"PA123456789BR"}]. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "message": "string",
      "sale": 1,
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `message` | string | Provider message for the tracking update item. |
| `sale` | number | Transaction code associated with the tracking update result. |
| `status` | string | Result status for the tracking update item. |

## Native endpoint

Through the native Monetizze API, this operation is `POST /sales/tracking` (base URL `https://api.monetizze.com.br/2.1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-sales-tracking.md) for the provider-specific parameters and requirements.

