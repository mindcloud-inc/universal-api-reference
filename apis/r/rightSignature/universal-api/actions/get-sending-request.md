# RightSignature: Get Sending Request

Retrieves a RightSignature sending request status.

```
GET https://connect.mindcloud.co/v1/universal/rightSignature/latest/actions/get-sending-request
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a RightSignature `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/rightSignature/latest/actions/get-sending-request?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/rightSignature/latest/actions/get-sending-request?${params}`, {
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
| `id` | string | yes | Sending Request id |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "2026-05-07T12:00:00.000Z",
      "documentTemplateId": "string",
      "id": "string",
      "status": "string",
      "statusMessage": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "uploadUrl": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | date |  |
| `documentTemplateId` | string |  |
| `id` | string |  |
| `status` | string |  |
| `statusMessage` | string |  |
| `updatedAt` | date |  |
| `uploadUrl` | string |  |

## Native endpoint

Through the native RightSignature API, this operation is `GET /sending_requests/:id` (base URL `https://api.rightsignature.com/public/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-sending-request.md) for the provider-specific parameters and requirements.

