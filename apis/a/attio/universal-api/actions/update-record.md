# Attio: Update Record

Updates a record in Attio.

```
PUT https://connect.mindcloud.co/v1/universal/attio/latest/actions/update-record
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Attio `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/attio/latest/actions/update-record" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "object": "string",
  "record_id": "string",
  "values": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/attio/latest/actions/update-record', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "object": "string",
    "record_id": "string",
    "values": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `object` | string | yes | The Attio object slug or UUID containing the record. |
| `record_id` | string | yes | The Attio record UUID to update. |
| `values` | object | yes | Record values keyed by Attio attribute slug or attribute ID. This overwrite endpoint replaces current multiselect values. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "2026-05-07T12:00:00.000Z",
      "id": {},
      "values": {},
      "webUrl": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | date | When the record was created. |
| `id` | object | Record identifier payload containing workspace, object, and record ids. |
| `values` | object | Dynamic attribute value payload for the record. |
| `webUrl` | string | Attio web URL for the record. |

## Native endpoint

Through the native Attio API, this operation is `PUT /v2/objects/:object/records/:record_id` (base URL `https://api.attio.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-record.md) for the provider-specific parameters and requirements.

