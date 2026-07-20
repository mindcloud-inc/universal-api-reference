# OpenRegister: Get Company Contact Information

Retrieves a company's contact information from OpenRegister.

```
GET https://connect.mindcloud.co/v1/universal/openRegister/latest/actions/get-company-contact-information
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a OpenRegister `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/openRegister/latest/actions/get-company-contact-information?connectionId=$CONNECTION_ID&companyId=DE-HRB-D2601-145602" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "companyId": "DE-HRB-D2601-145602"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/openRegister/latest/actions/get-company-contact-information?${params}`, {
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
| `companyId` | string | yes | Unique company identifier. Example: `DE-HRB-D2601-145602`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "email": "ava@example.com",
      "phone": "string",
      "source_url": "https://example.com",
      "vat_id": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `email` | string | Email address when available. |
| `phone` | string | Phone number when available. |
| `source_url` | string | Source URL for web contact data. |
| `vat_id` | string | VAT ID when available. |

## Native endpoint

Through the native OpenRegister API, this operation is `GET /v0/company/:company_id/contact` (base URL `https://api.openregister.de`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-company-contact-information.md) for the provider-specific parameters and requirements.

