# Billetto: Email BI Report

Sends a business intelligence report from Billetto by email.

```
POST https://connect.mindcloud.co/v1/universal/billetto/latest/actions/email-bi-report
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Billetto `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/billetto/latest/actions/email-bi-report" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "eventid": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/billetto/latest/actions/email-bi-report', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "eventid": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `eventid` | string | yes | Billetto event ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "object": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string |  |
| `object` | string |  |
| `status` | string |  |

## Native endpoint

Through the native Billetto API, this operation is `POST organiser/events/{eventid}/bi_report/by_email/` (base URL `https://billetto.dk/api/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/email-bi-report.md) for the provider-specific parameters and requirements.

