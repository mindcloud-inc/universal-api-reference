# WaiverForever: Get Waiver Request

Retrieves a waiver request from WaiverForever.

```
GET https://connect.mindcloud.co/v1/universal/waiverForever/latest/actions/get-waiver-request
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a WaiverForever `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/waiverForever/latest/actions/get-waiver-request?connectionId=$CONNECTION_ID&waiverRequestId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "waiverRequestId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/waiverForever/latest/actions/get-waiver-request?${params}`, {
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
| `includeWaivers` | boolean | no | Include submitted waivers in the response. |
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
      "type": "string",
      "waivers": [
        {}
      ]
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
| `waivers` | array<object> | Waivers submitted into this request group. |

## Native endpoint

Through the native WaiverForever API, this operation is `GET /openapi/v2/waiverRequest/:waiver_request_id` (base URL `https://api.waiverforever.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-waiver-request.md) for the provider-specific parameters and requirements.

