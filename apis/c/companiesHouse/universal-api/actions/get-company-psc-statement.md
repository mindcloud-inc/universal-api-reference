# Companies House: Get Company PSC Statement

Retrieves a person with significant control statement from Companies House.

```
GET https://connect.mindcloud.co/v1/universal/companiesHouse/latest/actions/get-company-psc-statement
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Companies House `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/companiesHouse/latest/actions/get-company-psc-statement?connectionId=$CONNECTION_ID&companyNumber=string&statementId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "companyNumber": "string",
  "statementId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/companiesHouse/latest/actions/get-company-psc-statement?${params}`, {
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
| `statementId` | string | yes | The PSC statement ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "ceased_on": "string",
      "etag": "string",
      "kind": "string",
      "linked_psc_name": "https://example.com",
      "links": {},
      "notified_on": "string",
      "restrictions_notice_withdrawal_reason": "string",
      "statement": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `ceased_on` | string |  |
| `etag` | string |  |
| `kind` | string |  |
| `linked_psc_name` | string |  |
| `links` | object |  |
| `notified_on` | string |  |
| `restrictions_notice_withdrawal_reason` | string |  |
| `statement` | string |  |

## Native endpoint

Through the native Companies House API, this operation is `GET /company/:company_number/persons-with-significant-control-statements/:statement_id` (base URL `https://api.company-information.service.gov.uk`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-company-psc-statement.md) for the provider-specific parameters and requirements.

