# Sign.Plus Universal API Examples

These examples use the MindCloud API key and Sign.Plus connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Envelopes



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/signPlus/latest/actions/list-envelopes?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/signPlus/latest/actions/list-envelopes?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

Example response:

```json
{
  "success": true,
  "data": [
    {
      "envelopes": [
        {}
      ],
      "has_next_page": true,
      "has_previous_page": true
    }
  ],
  "meta": {}
}
```

See the full [List Envelopes action reference](actions/list-envelopes.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/signPlus/latest/actions/list-envelopes).

## Add Envelope Annotation



```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/signPlus/latest/actions/add-envelope-annotation" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "envelopeId": "string",
  "recipientId": "string",
  "documentId": "string",
  "page": 1,
  "x": 1,
  "y": 1,
  "width": 1,
  "height": 1,
  "required": true,
  "type": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/signPlus/latest/actions/add-envelope-annotation', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "envelopeId": "string",
    "recipientId": "string",
    "documentId": "string",
    "page": 1,
    "x": 1,
    "y": 1,
    "width": 1,
    "height": 1,
    "required": true,
    "type": "string"
  })
});

const { success, data } = await response.json();
```

Example response:

```json
{
  "success": true,
  "data": [
    {
      "checkbox": {},
      "datetime": {},
      "document_id": "string",
      "height": 1,
      "id": "string",
      "initials": {},
      "page": 1,
      "recipient_id": "string",
      "required": true,
      "signature": {},
      "text": {},
      "type": "string",
      "width": 1,
      "x": 1,
      "y": 1
    }
  ],
  "meta": {}
}
```

See the full [Add Envelope Annotation action reference](actions/add-envelope-annotation.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/signPlus/latest/actions/add-envelope-annotation).
