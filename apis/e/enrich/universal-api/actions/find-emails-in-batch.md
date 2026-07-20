# Enrich.so: Find Emails in Batch

Creates a batch email finder job in Enrich.so.

```
POST https://connect.mindcloud.co/v1/universal/enrich/latest/actions/find-emails-in-batch
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Enrich.so `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/enrich/latest/actions/find-emails-in-batch" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "leads[]": [
    {
      "domain": "stripe.com",
      "lastName": "Chen",
      "firstName": "Sarah"
    }
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/enrich/latest/actions/find-emails-in-batch', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "leads[]": [{"domain":"stripe.com","lastName":"Chen","firstName":"Sarah"}]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `leads[]` | array<object> | yes | Lead objects containing firstName, lastName, and domain. Default: `[{"domain":"stripe.com","lastName":"Chen","firstName":"Sarah"}]`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `webhookUrl` | string | no | Optional callback URL for batch completion. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "batchId": "string",
      "duplicatesRemoved": 1,
      "itemCount": 1,
      "originalCount": 1,
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `batchId` | string | Batch identifier returned for the email finder job. |
| `duplicatesRemoved` | number | Number of duplicate leads removed. |
| `itemCount` | number | Number of unique leads accepted. |
| `originalCount` | number | Number of submitted leads before deduplication. |
| `status` | string | Initial batch status. |

## Native endpoint

Through the native Enrich.so API, this operation is `POST /email-finder/batch` (base URL `https://dev.enrich.so/api/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/find-emails-in-batch.md) for the provider-specific parameters and requirements.

