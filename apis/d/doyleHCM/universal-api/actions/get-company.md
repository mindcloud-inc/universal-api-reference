# Doyle HCM: Get company

Retrieves a company from Doyle HCM by ID.

```
GET https://connect.mindcloud.co/v1/universal/doyleHCM/latest/actions/get-company
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Doyle HCM `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/doyleHCM/latest/actions/get-company?connectionId=$CONNECTION_ID&companyId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "companyId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/doyleHCM/latest/actions/get-company?${params}`, {
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
      "blocked": true,
      "companyAddress": {},
      "companyType": 1,
      "createdOn": "string",
      "email": "ava@example.com",
      "enabledEWA": true,
      "enabledUnions": true,
      "externalId": "string",
      "fein": "string",
      "id": 1,
      "name": "Ava Chen",
      "refCode": "string",
      "reqEEJobCostCode": true,
      "startOn": "string",
      "timeZone": 1,
      "tradeName": "Ava Chen",
      "uiNumber": 1,
      "website": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `blocked` | boolean | Whether the company is blocked. |
| `companyAddress` | object | Company address block when returned. |
| `companyType` | number | Company type code. |
| `createdOn` | string | Company creation timestamp when available. |
| `email` | string | Primary company email when returned. |
| `enabledEWA` | boolean | Whether earned wage access is enabled. |
| `enabledUnions` | boolean | Whether unions are enabled. |
| `externalId` | string | External company identifier when returned. |
| `fein` | string | Federal employer identification number when returned. |
| `id` | number | Company identifier. |
| `name` | string | Company display name. |
| `refCode` | string | Reference code when returned. |
| `reqEEJobCostCode` | boolean | Whether employee job cost code is required. |
| `startOn` | string | Company start date when available. |
| `timeZone` | number | Time zone code when returned. |
| `tradeName` | string | Trade name when available. |
| `uiNumber` | number | State unemployment insurance number when returned. |
| `website` | string | Company website URL when returned. |

## Native endpoint

Through the native Doyle HCM API, this operation is `GET /wep/companies/:companyId` (base URL `https://api.worklio.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-company.md) for the provider-specific parameters and requirements.

