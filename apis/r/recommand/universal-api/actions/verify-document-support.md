# Recommand: Verify Document Support

Verifies document support for a Recommand recipient.

```
GET https://connect.mindcloud.co/v1/universal/recommand/latest/actions/verify-document-support
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Recommand `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/recommand/latest/actions/verify-document-support?connectionId=$CONNECTION_ID&documenttype=string&peppoladdress=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "documenttype": "string",
  "peppoladdress": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/recommand/latest/actions/verify-document-support?${params}`, {
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
| `documenttype` | string | yes | The document type to verify. You can use a full document type ID, or the simplified versions (e.g. "invoice", "creditNote", "selfBillingInvoice", "selfBillingCreditNote", ...). |
| `peppoladdress` | string | yes | The Peppol address of the recipient to verify. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "certificateExpiry": "string",
      "isValid": true,
      "serviceEndpoint": "string",
      "serviceProvider": "string",
      "smpUrl": "https://example.com",
      "success": true,
      "technicalContact": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `certificateExpiry` | string |  |
| `isValid` | boolean |  |
| `serviceEndpoint` | string |  |
| `serviceProvider` | string |  |
| `smpUrl` | string |  |
| `success` | boolean |  |
| `technicalContact` | string |  |

## Native endpoint

Through the native Recommand API, this operation is `POST /api/v1/verify-document-support` (base URL `https://app.recommand.eu`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/verify-document-support.md) for the provider-specific parameters and requirements.

