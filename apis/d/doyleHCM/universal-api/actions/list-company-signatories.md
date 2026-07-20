# Doyle HCM: List company signatories

Retrieves company signatories from Doyle HCM.

```
GET https://connect.mindcloud.co/v1/universal/doyleHCM/latest/actions/list-company-signatories
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Doyle HCM `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/doyleHCM/latest/actions/list-company-signatories?connectionId=$CONNECTION_ID&companyId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "companyId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/doyleHCM/latest/actions/list-company-signatories?${params}`, {
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
| `companyId` | number | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "addressCity": "string",
      "addressCountry": "string",
      "addressLine1": "string",
      "addressLine2": "string",
      "addressState": "string",
      "addressZIP": "string",
      "birthDate": "string",
      "documents": [
        {}
      ],
      "email": "ava@example.com",
      "firstName": "Ava",
      "id": 1,
      "lastName": "Chen",
      "phone": "string",
      "position": "string",
      "ssnMasked": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `addressCity` | string | Address city when returned. |
| `addressCountry` | string | Address country when returned. |
| `addressLine1` | string | Address line 1 when returned. |
| `addressLine2` | string | Address line 2 when returned. |
| `addressState` | string | Address state when returned. |
| `addressZIP` | string | Address postal code when returned. |
| `birthDate` | string | Birth date timestamp when returned. |
| `documents` | array<object> | Proof documents attached to the signatory when returned. |
| `email` | string | Personal email for the signatory when returned. |
| `firstName` | string | Signatory first name when returned. |
| `id` | number | Signatory identifier. |
| `lastName` | string | Signatory last name when returned. |
| `phone` | string | Personal phone for the signatory when returned. |
| `position` | string | Signatory company position when returned. |
| `ssnMasked` | string | Masked SSN for the signatory when returned. |

## Native endpoint

Through the native Doyle HCM API, this operation is `GET /wep/companies/:companyId/signatories` (base URL `https://api.worklio.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-company-signatories.md) for the provider-specific parameters and requirements.

