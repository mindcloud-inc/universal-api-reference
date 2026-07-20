# Clicksign: List Document Events

Retrieves events for a Clicksign document.

```
GET https://connect.mindcloud.co/v1/universal/clicksign/latest/actions/list-document-events
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Clicksign `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/clicksign/latest/actions/list-document-events?connectionId=$CONNECTION_ID&documentId=string&envelopeId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "documentId": "string",
  "envelopeId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/clicksign/latest/actions/list-document-events?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `documentId` | string | yes | The UUID of the document. |
| `envelopeId` | string | yes | The UUID of the envelope. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Clicksign API returns.

## Native endpoint

Through the native Clicksign API, this operation is `GET /envelopes/:envelope_id/documents/:document_id/events` (base URL `https://app.clicksign.com/api/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-document-events.md) for the provider-specific parameters and requirements.

