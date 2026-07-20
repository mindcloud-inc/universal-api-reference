# Skribble Sign: Get Signature Request Report

Retrieves a signature request report from Skribble Sign.

```
GET https://connect.mindcloud.co/v1/universal/skribbleSign/latest/actions/get-signature-request-report
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Skribble Sign `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/skribbleSign/latest/actions/get-signature-request-report?connectionId=$CONNECTION_ID&signatureRequestId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "signatureRequestId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/skribbleSign/latest/actions/get-signature-request-report?${params}`, {
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
| `signatureRequestId` | string | yes | The signature request ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": [
        1
      ],
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | array<number> | Signature request report bytes. |
| `type` | string | Raw response wrapper type. |

## Native endpoint

Through the native Skribble Sign API, this operation is `GET /v2/signature-requests/:signatureRequestId/report` (base URL `https://api.skribble.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-signature-request-report.md) for the provider-specific parameters and requirements.

