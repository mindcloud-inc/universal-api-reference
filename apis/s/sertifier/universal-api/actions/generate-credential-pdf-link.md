# Sertifier: Generate Credential PDF Link

Retrieves a credential PDF link from Sertifier.

```
GET https://connect.mindcloud.co/v1/universal/sertifier/latest/actions/generate-credential-pdf-link
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Sertifier `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sertifier/latest/actions/generate-credential-pdf-link?connectionId=$CONNECTION_ID&credential_id_OR_certificate_no=Credential%20ID%20or%20certificate%20number" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "credential_id_OR_certificate_no": "Credential ID or certificate number"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sertifier/latest/actions/generate-credential-pdf-link?${params}`, {
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
| `credential_id_OR_certificate_no` | string | yes | Example: `Credential ID or certificate number`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "link": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `link` | string |  |

## Native endpoint

Through the native Sertifier API, this operation is `GET /credential/generatePDFLink/:credential_id_OR_certificate_no` (base URL `https://b2b.sertifier.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/generate-credential-pdf-link.md) for the provider-specific parameters and requirements.

