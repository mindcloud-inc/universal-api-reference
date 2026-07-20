# OpenRegister: Get Company

Retrieves company information from OpenRegister by company ID.

```
GET https://connect.mindcloud.co/v1/universal/openRegister/latest/actions/get-company
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a OpenRegister `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/openRegister/latest/actions/get-company?connectionId=$CONNECTION_ID&companyId=DE-HRB-D2601-145602" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "companyId": "DE-HRB-D2601-145602"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/openRegister/latest/actions/get-company?${params}`, {
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

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `realtime` | boolean | no | Fetch latest Handelsregister data when true. Increases credit cost. Default: `false`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "address": {},
      "documents": [
        {}
      ],
      "id": "string",
      "legal_form": "string",
      "name": {},
      "representation": [
        {}
      ],
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `address` | object | Current company address object. |
| `documents` | array<object> | Stored company documents. |
| `id` | string | Company ID. |
| `legal_form` | string | Company legal form. |
| `name` | object | Current company name object. |
| `representation` | array<object> | Company representation people. |
| `status` | string | Company status. |

## Native endpoint

Through the native OpenRegister API, this operation is `GET /v1/company/:company_id` (base URL `https://api.openregister.de`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-company.md) for the provider-specific parameters and requirements.

