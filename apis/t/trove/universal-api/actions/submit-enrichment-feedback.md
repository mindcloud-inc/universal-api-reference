# Trove: Submit Enrichment Feedback

Submits transaction enrichment feedback to Trove.

```
PUT https://connect.mindcloud.co/v1/universal/trove/latest/actions/submit-enrichment-feedback
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Trove `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/trove/latest/actions/submit-enrichment-feedback" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "description": "string",
  "domain": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/trove/latest/actions/submit-enrichment-feedback', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "description": "string",
    "domain": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `description` | string | yes | The original transaction description previously sent to Enrich Transaction. |
| `domain` | string | yes | The correct domain to associate with the transaction description. |
| `comment` | string | no | Optional feedback about the enrichment response. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "success": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `success` | string | Feedback submission confirmation message from Trove. |

## Native endpoint

Through the native Trove API, this operation is `POST /transactions/feedback` (base URL `https://trove.headline.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/submit-enrichment-feedback.md) for the provider-specific parameters and requirements.

