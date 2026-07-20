# Sign.Plus: Get Signed Document



```
GET https://connect.mindcloud.co/v1/universal/signPlus/latest/actions/get-signed-document
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Sign.Plus `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/signPlus/latest/actions/get-signed-document?connectionId=$CONNECTION_ID&envelopeId=string&documentId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "envelopeId": "string",
  "documentId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/signPlus/latest/actions/get-signed-document?${params}`, {
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
| `envelopeId` | string | yes |  |
| `documentId` | string | yes |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Sign.Plus API returns.

## Native endpoint

Through the native Sign.Plus API, this operation is `GET /envelope/:envelope_id/signed_documents/:document_id` (base URL `https://restapi.sign.plus/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-signed-document.md) for the provider-specific parameters and requirements.

