# Doyle HCM: List company KYC document types

Retrieves company KYC document types from Doyle HCM.

```
GET https://connect.mindcloud.co/v1/universal/doyleHCM/latest/actions/list-company-kyc-document-types
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Doyle HCM `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/doyleHCM/latest/actions/list-company-kyc-document-types?connectionId=$CONNECTION_ID&companyId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "companyId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/doyleHCM/latest/actions/list-company-kyc-document-types?${params}`, {
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
      "description": "string",
      "fileTypes": "string",
      "isFile": true,
      "isRequired": true,
      "isSecondary": true,
      "key": "string",
      "name": "Ava Chen",
      "scope": 1,
      "trustLevel": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `description` | string | Document type description. |
| `fileTypes` | string | Accepted file type list when returned. |
| `isFile` | boolean | Whether the document type expects a file upload. |
| `isRequired` | boolean | Whether the document type is required. |
| `isSecondary` | boolean | Whether the document type is secondary. |
| `key` | string | Document type key. |
| `name` | string | Document type display name. |
| `scope` | number | Document scope code. |
| `trustLevel` | number | Trust level code for the document type. |

## Native endpoint

Through the native Doyle HCM API, this operation is `GET /wep/companies/:companyId/kyc/documenttypes` (base URL `https://api.worklio.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-company-kyc-document-types.md) for the provider-specific parameters and requirements.

