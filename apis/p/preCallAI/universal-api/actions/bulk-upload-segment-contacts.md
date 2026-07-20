# PreCallAI: Bulk Upload Segment Contacts

Bulk uploads segment contacts in PreCallAI.

```
POST https://connect.mindcloud.co/v1/universal/preCallAI/latest/actions/bulk-upload-segment-contacts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PreCallAI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/preCallAI/latest/actions/bulk-upload-segment-contacts" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/preCallAI/latest/actions/bulk-upload-segment-contacts', {
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

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | no | The segment ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {},
      "message": "string",
      "status": 1,
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | object | Optional provider payload returned for the bulk upload. |
| `message` | string | Provider status message for the bulk upload. |
| `status` | number | HTTP-style status returned by PreCallAI. |
| `success` | boolean | Whether the bulk upload request succeeded. |

## Native endpoint

Through the native PreCallAI API, this operation is `POST /segment/contact/bulk-upload` (base URL `https://api.precallai.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/bulk-upload-segment-contacts.md) for the provider-specific parameters and requirements.

