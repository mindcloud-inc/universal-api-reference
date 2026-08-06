# Avalara AvaTax: Get Company



```
GET https://connect.mindcloud.co/v1/universal/avalara/latest/actions/get-company
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Avalara AvaTax `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/avalara/latest/actions/get-company?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/avalara/latest/actions/get-company?${params}`, {
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
| `id` | number | yes | Avalara company ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "accountId": 1,
      "companyCode": "string",
      "createdDate": "2026-05-07T12:00:00.000Z",
      "createdUserId": 1,
      "defaultCountry": "string",
      "hasProfile": true,
      "id": 1,
      "inProgress": true,
      "isActive": true,
      "isAdvSave": true,
      "isDefault": true,
      "isDeleted": true,
      "isFein": true,
      "isReportingEntity": true,
      "isTest": true,
      "modifiedDate": "2026-05-07T12:00:00.000Z",
      "modifiedUserId": 1,
      "name": "Ava Chen",
      "parentCompanyId": 1,
      "roundingLevelId": "string",
      "taxDependencyLevelId": "string",
      "taxpayerIdNumber": "string",
      "warningsEnabled": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accountId` | number | AvaTax account ID. |
| `companyCode` | string | Company code. |
| `createdDate` | date | Creation timestamp. |
| `createdUserId` | number | User ID that created the company. |
| `defaultCountry` | string | Default country code. |
| `hasProfile` | boolean | Whether the company has a tax profile. |
| `id` | number | AvaTax company ID. |
| `inProgress` | boolean | Whether the company setup is in progress. |
| `isActive` | boolean | Whether the company is active. |
| `isAdvSave` | boolean | Whether advanced save is enabled. |
| `isDefault` | boolean | Whether this is the default company. |
| `isDeleted` | boolean | Whether the company is deleted. |
| `isFein` | boolean | Whether the taxpayer ID is a FEIN. |
| `isReportingEntity` | boolean | Whether the company is the reporting entity. |
| `isTest` | boolean | Whether the company is marked as test. |
| `modifiedDate` | date | Last modification timestamp. |
| `modifiedUserId` | number | User ID that last modified the company. |
| `name` | string | Company name. |
| `parentCompanyId` | number | Parent company ID when applicable. |
| `roundingLevelId` | string | Rounding level identifier. |
| `taxDependencyLevelId` | string | Tax dependency level identifier. |
| `taxpayerIdNumber` | string | Taxpayer identification number. |
| `warningsEnabled` | boolean | Whether warnings are enabled. |

## Native endpoint

Through the native Avalara AvaTax API, this operation is `GET companies/:id` (base URL `{{credentials.environment}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-company.md) for the provider-specific parameters and requirements.

