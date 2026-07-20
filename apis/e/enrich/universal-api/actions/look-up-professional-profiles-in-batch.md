# Enrich.so: Look Up Professional Profiles in Batch

Creates a bulk profile lookup job in Enrich.so.

```
POST https://connect.mindcloud.co/v1/universal/enrich/latest/actions/look-up-professional-profiles-in-batch
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Enrich.so `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/enrich/latest/actions/look-up-professional-profiles-in-batch" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "emails[]": [
    "sarah.chen@stripe.com"
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/enrich/latest/actions/look-up-professional-profiles-in-batch', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "emails[]": ["sarah.chen@stripe.com"]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `emails[]` | array<string> | yes | Email addresses to look up in the bulk profile lookup job. Default: `["sarah.chen@stripe.com"]`. |

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
| `batchId` | string | Bulk reverse lookup batch identifier. |
| `duplicatesRemoved` | number | Number of duplicate emails removed. |
| `itemCount` | number | Number of emails accepted. |
| `originalCount` | number | Number of submitted emails before deduplication. |
| `status` | string | Initial batch status. |

## Native endpoint

Through the native Enrich.so API, this operation is `POST /reverse-lookup/bulk-lookup` (base URL `https://dev.enrich.so/api/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/look-up-professional-profiles-in-batch.md) for the provider-specific parameters and requirements.

