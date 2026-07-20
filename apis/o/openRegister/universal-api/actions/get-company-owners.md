# OpenRegister: Get Company Owners

Retrieves a company's owners from OpenRegister.

```
GET https://connect.mindcloud.co/v1/universal/openRegister/latest/actions/get-company-owners
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a OpenRegister `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/openRegister/latest/actions/get-company-owners?connectionId=$CONNECTION_ID&companyId=DE-HRB-D2601-145602" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "companyId": "DE-HRB-D2601-145602"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/openRegister/latest/actions/get-company-owners?${params}`, {
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
      "company_id": "string",
      "owners": [
        {}
      ],
      "sources": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `company_id` | string | Company ID. |
| `owners` | array<object> | Current company owners. |
| `sources` | array<object> | Source documents. |

## Native endpoint

Through the native OpenRegister API, this operation is `GET /v1/company/:company_id/owners` (base URL `https://api.openregister.de`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-company-owners.md) for the provider-specific parameters and requirements.

