# Lumin: Update Signature Request



```
PUT https://connect.mindcloud.co/v1/universal/lumin/latest/actions/update-signature-request
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Lumin `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/lumin/latest/actions/update-signature-request" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "signatureRequestId": "string",
  "expiresAt": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/lumin/latest/actions/update-signature-request', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "signatureRequestId": "string",
    "expiresAt": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `signatureRequestId` | string | yes | ID of the signature request. |
| `expiresAt` | number | yes | Future Unix timestamp in milliseconds. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "signatureRequest": {
        "createdAt": 1,
        "detailsUrl": "https://example.com",
        "expiresAt": 1,
        "signatureRequestId": "string",
        "signers": [
          {
            "email": "ava@example.com",
            "group": 1,
            "isApproved": true,
            "name": "Ava Chen",
            "status": "string"
          }
        ],
        "signingType": "string",
        "status": "string",
        "title": "string",
        "updatedAt": 1
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `signatureRequest.createdAt` | number |  |
| `signatureRequest.detailsUrl` | string |  |
| `signatureRequest.expiresAt` | number |  |
| `signatureRequest.signatureRequestId` | string |  |
| `signatureRequest.signers[].email` | string |  |
| `signatureRequest.signers[].group` | number |  |
| `signatureRequest.signers[].isApproved` | boolean |  |
| `signatureRequest.signers[].name` | string |  |
| `signatureRequest.signers[].status` | string |  |
| `signatureRequest.signingType` | string |  |
| `signatureRequest.status` | string |  |
| `signatureRequest.title` | string |  |
| `signatureRequest.updatedAt` | number |  |

## Native endpoint

Through the native Lumin API, this operation is `PATCH /signature_request/:signature_request_id` (base URL `https://api.luminpdf.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-signature-request.md) for the provider-specific parameters and requirements.

