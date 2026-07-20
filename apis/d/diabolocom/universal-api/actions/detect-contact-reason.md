# Diabolocom: Detect Contact Reason

Creates a contact reason detection job in Diabolocom.

```
POST https://connect.mindcloud.co/v1/universal/diabolocom/latest/actions/detect-contact-reason
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Diabolocom `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/diabolocom/latest/actions/detect-contact-reason" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/diabolocom/latest/actions/detect-contact-reason', {
  method: 'POST',
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



## Response

```json
{
  "success": true,
  "data": [
    {
      "correlation_id": "string",
      "job_id": "string",
      "job_status_endpoint_url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `correlation_id` | string |  |
| `job_id` | string |  |
| `job_status_endpoint_url` | string |  |

## Native endpoint

Through the native Diabolocom API, this operation is `POST /api/job/text-tasks` (base URL `https://api.diabolocom.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/detect-contact-reason.md) for the provider-specific parameters and requirements.

