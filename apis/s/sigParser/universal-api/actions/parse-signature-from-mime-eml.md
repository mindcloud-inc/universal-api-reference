# SigParser: Parse Signature From MIME/EML



```
GET https://connect.mindcloud.co/v1/universal/sigParser/latest/actions/parse-signature-from-mime-eml
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SigParser `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sigParser/latest/actions/parse-signature-from-mime-eml?connectionId=$CONNECTION_ID&mimeFile=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "mimeFile": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sigParser/latest/actions/parse-signature-from-mime-eml?${params}`, {
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
| `mimeFile` | file | yes | Upload the MIME or EML file contents for the email to parse. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "address": "string",
      "addressParts": {},
      "companyName": "Ava Chen",
      "duration": 1,
      "errors": [
        "string"
      ],
      "fromAddress": "string",
      "fromDisplayname": "Ava Chen",
      "jobTitle": "string",
      "links": [
        {}
      ],
      "phones": [
        {}
      ],
      "signature": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `address` | string | Full address extracted from the signature. |
| `addressParts` | object | Structured address parts extracted from the signature. |
| `companyName` | string | Best-matched company name from the signature. |
| `duration` | number | Processing duration in milliseconds. |
| `errors` | array<string> | Any parse warnings or errors returned by SigParser. |
| `fromAddress` | string | Email address of the sender of the email. |
| `fromDisplayname` | string | Display name for the sender of the email. |
| `jobTitle` | string | Job title parsed from the signature. |
| `links` | array<object> | Links extracted from the signature. |
| `phones` | array<object> | Phone numbers extracted from the signature. |
| `signature` | string | Signature text extracted from the email. |

## Native endpoint

Through the native SigParser API, this operation is `POST /api/Parse/Email/Contact/MIME` (base URL `https://ipaas.sigparser.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/parse-signature-from-mime-eml.md) for the provider-specific parameters and requirements.

