# edatalia Sign Online: Timestamp Signed PDF

Adds a timestamp to a signed PDF in edatalia Sign Online.

```
POST https://connect.mindcloud.co/v1/universal/edataliaSignOnline/latest/actions/timestamp-signed-pdf
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a edatalia Sign Online `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/edataliaSignOnline/latest/actions/timestamp-signed-pdf" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "b64PDFContent": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/edataliaSignOnline/latest/actions/timestamp-signed-pdf', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "b64PDFContent": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `b64PDFContent` | string | yes | Signed PDF document content encoded as base64. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `timestampProvider` | object | no | Optional external timestamp provider settings. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "content": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `content` | string | Timestamped PDF content returned by the API. |

## Native endpoint

Through the native edatalia Sign Online API, this operation is `POST /eSign/v40/Signature/Timestamp` (base URL `https://restapi.firmar.online`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/timestamp-signed-pdf.md) for the provider-specific parameters and requirements.

