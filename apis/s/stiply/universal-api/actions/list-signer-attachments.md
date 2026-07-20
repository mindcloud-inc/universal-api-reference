# Stiply: List Signer Attachments

Retrieves signer attachments for a Stiply sign request.

```
GET https://connect.mindcloud.co/v1/universal/stiply/latest/actions/list-signer-attachments
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Stiply `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/stiply/latest/actions/list-signer-attachments?connectionId=$CONNECTION_ID&signRequest=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "signRequest": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/stiply/latest/actions/list-signer-attachments?${params}`, {
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
| `signRequest` | number | yes | Id of the signrequest. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "description": "string",
      "hasDocument": true,
      "id": 1,
      "identityInformation": "string",
      "optional": true,
      "signerId": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `description` | string |  |
| `hasDocument` | boolean |  |
| `id` | number |  |
| `identityInformation` | string |  |
| `optional` | boolean |  |
| `signerId` | number |  |

## Native endpoint

Through the native Stiply API, this operation is `GET /v2/sign_requests/:sign_request/signer_attachments` (base URL `https://api.stiply.nl`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-signer-attachments.md) for the provider-specific parameters and requirements.

