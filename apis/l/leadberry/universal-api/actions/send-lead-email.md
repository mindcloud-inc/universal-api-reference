# Leadberry: Send Lead Email



```
POST https://connect.mindcloud.co/v1/universal/leadberry/latest/actions/send-lead-email
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Leadberry `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/leadberry/latest/actions/send-lead-email" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "address": "string",
  "visibleUrlId": "https://example.com",
  "date": "2026-05-07T12:00:00.000Z",
  "source": "string",
  "country": "string",
  "landingPagePath": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/leadberry/latest/actions/send-lead-email', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "address": "string",
    "visibleUrlId": "https://example.com",
    "date": "2026-05-07T12:00:00.000Z",
    "source": "string",
    "country": "string",
    "landingPagePath": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `address` | string | yes | Email address to send the Leadberry lead email to. |
| `visibleUrlId` | string | yes | Leadberry visible URL identifier for the target lead. |
| `date` | date | yes | Lead date associated with the email. |
| `source` | string | yes | Lead source string from Leadberry result data. |
| `country` | string | yes | Lead country value. |
| `landingPagePath` | string | yes | Landing page path visited by the lead. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `deepContacts` | string | no | JSON-stringified deep contacts payload when available. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Leadberry API returns.

## Native endpoint

Through the native Leadberry API, this operation is `POST /data/sendLeadEmail` (base URL `https://app.leadberry.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/send-lead-email.md) for the provider-specific parameters and requirements.

