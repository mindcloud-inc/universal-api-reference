# WaiverForever: Create Waiver Request

Creates a waiver request in WaiverForever.

```
POST https://connect.mindcloud.co/v1/universal/waiverForever/latest/actions/create-waiver-request
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a WaiverForever `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/waiverForever/latest/actions/create-waiver-request" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen",
  "size": 1,
  "templateId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/waiverForever/latest/actions/create-waiver-request', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Ava Chen",
    "size": 1,
    "templateId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `contactInfo` | string | no | Optional contact information for the request group. |
| `name` | string | yes | Waiver request group name. |
| `note` | string | no | Optional request note. |
| `size` | number | yes | Number of recipients to create in the request group. |
| `templateId` | string | yes | Template used by the waiver request. |
| `type` | string | no | Request type such as normal or anonymous. |

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

Through the native WaiverForever API, this operation is `POST /openapi/v2/waiverRequest` (base URL `https://api.waiverforever.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-waiver-request.md) for the provider-specific parameters and requirements.

