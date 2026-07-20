# Companies House: Get Company PSC Super Secure Beneficial Owner

Retrieves a super secure beneficial owner notification from Companies House.

```
GET https://connect.mindcloud.co/v1/universal/companiesHouse/latest/actions/get-company-psc-super-secure-beneficial-owner
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Companies House `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/companiesHouse/latest/actions/get-company-psc-super-secure-beneficial-owner?connectionId=$CONNECTION_ID&companyNumber=string&superSecureId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "companyNumber": "string",
  "superSecureId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/companiesHouse/latest/actions/get-company-psc-super-secure-beneficial-owner?${params}`, {
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
| `companyNumber` | string | yes | The company number. |
| `superSecureId` | string | yes | The super secure beneficial owner ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "ceased": true,
      "description": "string",
      "etag": "string",
      "kind": "string",
      "links": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `ceased` | boolean |  |
| `description` | string |  |
| `etag` | string |  |
| `kind` | string |  |
| `links` | object |  |

## Native endpoint

Through the native Companies House API, this operation is `GET /company/:company_number/persons-with-significant-control/super-secure-beneficial-owner/:super_secure_id` (base URL `https://api.company-information.service.gov.uk`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-company-psc-super-secure-beneficial-owner.md) for the provider-specific parameters and requirements.

