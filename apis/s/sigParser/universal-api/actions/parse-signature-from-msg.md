# SigParser: Parse Signature From MSG



```
GET https://connect.mindcloud.co/v1/universal/sigParser/latest/actions/parse-signature-from-msg
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SigParser `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sigParser/latest/actions/parse-signature-from-msg?connectionId=$CONNECTION_ID&msgFile=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "msgFile": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sigParser/latest/actions/parse-signature-from-msg?${params}`, {
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
| `msgFile` | file | yes | Upload the MSG file contents for the email to parse. |

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
| `address` | string | Parsed mailing address. |
| `addressParts` | object | Structured address parts. |
| `companyName` | string | Parsed company name. |
| `duration` | number | Processing duration in milliseconds. |
| `errors` | array<string> | Parsing errors returned by SigParser. |
| `fromAddress` | string | Parsed sender email address. |
| `fromDisplayname` | string | Parsed sender display name. |
| `jobTitle` | string | Parsed job title. |
| `links` | array<object> | Parsed links found in the signature. |
| `phones` | array<object> | Parsed phone numbers. |
| `signature` | string | Normalized email signature text. |

## Native endpoint

Through the native SigParser API, this operation is `POST /api/Parse/Email/Contact/MSG` (base URL `https://ipaas.sigparser.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/parse-signature-from-msg.md) for the provider-specific parameters and requirements.

