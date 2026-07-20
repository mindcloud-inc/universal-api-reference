# WaiverForever: Edit Waiver Request

Updates a waiver request in WaiverForever.

```
PUT https://connect.mindcloud.co/v1/universal/waiverForever/latest/actions/edit-waiver-request
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a WaiverForever `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/waiverForever/latest/actions/edit-waiver-request" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen",
  "size": 1,
  "waiverRequestId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/waiverForever/latest/actions/edit-waiver-request', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Ava Chen",
    "size": 1,
    "waiverRequestId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `contactInfo` | string | no | Updated contact information. |
| `name` | string | yes | Updated waiver request group name. |
| `note` | string | no | Updated request note. |
| `size` | number | yes | Updated request group size. |
| `waiverRequestId` | string | yes | Waiver request group identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "acceptedCount": 1,
      "contactInfo": "string",
      "datetime": 1,
      "id": "string",
      "name": "Ava Chen",
      "note": "string",
      "requestLink": "https://example.com",
      "size": 1,
      "status": "string",
      "submittedCount": 1,
      "templateId": "string",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `acceptedCount` | number | Number of accepted request slots. |
| `contactInfo` | string | Contact information stored on the request. |
| `datetime` | number | Created timestamp. |
| `id` | string | Waiver request identifier. |
| `name` | string | Waiver request name. |
| `note` | string | Waiver request note. |
| `requestLink` | string | Share link for the waiver request. |
| `size` | number | Number of recipients in the request group. |
| `status` | string | Waiver request status. |
| `submittedCount` | number | Number of submitted waivers. |
| `templateId` | string | Template used for the waiver request. |
| `type` | string | Waiver request type. |

## Native endpoint

Through the native WaiverForever API, this operation is `POST /openapi/v2/waiverRequest/:waiver_request_id` (base URL `https://api.waiverforever.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/edit-waiver-request.md) for the provider-specific parameters and requirements.

