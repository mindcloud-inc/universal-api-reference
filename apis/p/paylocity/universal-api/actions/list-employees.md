# Paylocity: List Employees

Retrieves the list of employees of a company

```
GET https://connect.mindcloud.co/v1/universal/paylocity/latest/actions/list-employees
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Paylocity `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/paylocity/latest/actions/list-employees?connectionId=$CONNECTION_ID&limit=25&offset=0&companyId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "companyId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/paylocity/latest/actions/list-employees?${params}`, {
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
| `companyId` | string | yes | Id of the company that is being accessed |
| `include` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "address": {
        "country": "string",
        "county": "string",
        "label": "string",
        "line1": "string",
        "locality": "string",
        "postalCode": "string",
        "state": "string",
        "type": "string"
      },
      "clientId": 1,
      "companyId": "string",
      "dba": "string",
      "ein": "string",
      "entityType": "string",
      "industryType": "string",
      "naics": 1,
      "parentCompanySetId": "string",
      "phone": "string",
      "relationships": [
        {
          "description": "string",
          "relationshipType": "string"
        }
      ],
      "serviceStartDate": "string",
      "status": "string",
      "webTimeCo": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `address.country` | string |  |
| `address.county` | string |  |
| `address.label` | string |  |
| `address.line1` | string |  |
| `address.locality` | string |  |
| `address.postalCode` | string |  |
| `address.state` | string |  |
| `address.type` | string |  |
| `clientId` | number |  |
| `companyId` | string |  |
| `dba` | string |  |
| `ein` | string |  |
| `entityType` | string |  |
| `industryType` | string |  |
| `naics` | number |  |
| `parentCompanySetId` | string |  |
| `phone` | string |  |
| `relationships[].description` | string |  |
| `relationships[].relationshipType` | string |  |
| `serviceStartDate` | string |  |
| `status` | string |  |
| `webTimeCo` | string |  |

## Native endpoint

Through the native Paylocity API, this operation is `GET coreHr/v1/companies/:companyId/employees` (base URL `{{credentials.connection}}`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-employees.md) for the provider-specific parameters and requirements.

