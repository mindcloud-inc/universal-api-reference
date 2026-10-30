# ServiceTitan: Get Payroll Adjustments

Retrieves payroll adjustments from ServiceTitan.

```
GET https://connect.mindcloud.co/v1/universal/servicetitan/latest/actions/get-payroll-adjustments
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ServiceTitan `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/servicetitan/latest/actions/get-payroll-adjustments?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/servicetitan/latest/actions/get-payroll-adjustments?${params}`, {
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
| `employeeIds` | string | no | Comma-separated employee or technician IDs, such as 123,456. Accepts multiple values in one string, delimited by `,`. |
| `postedOnOrAfter` | date | no | Return adjustments posted on or after this UTC date and time. Example: `2026-01-15T00:00:00Z`. |
| `postedOnOrBefore` | date | no | Return adjustments posted on or before this UTC date and time. Example: `2026-01-15T00:00:00Z`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `active` | list<string> | no | One of: `Any`, `False`, `True`. Default: `True`. |
| `createdBefore` | date | no | Example: `2026-01-15T00:00:00Z`. |
| `createdOnOrAfter` | date | no | Example: `2026-01-15T00:00:00Z`. |
| `modifiedBefore` | date | no | Example: `2026-01-15T00:00:00Z`. |
| `modifiedOnOrAfter` | date | no | Example: `2026-01-15T00:00:00Z`. |
| `includeTotal` | boolean | no |  |
| `sort` | string | no | Sort expression accepted by ServiceTitan. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "active": true,
      "activityCodeId": 1,
      "amount": 1,
      "businessUnitId": 1,
      "createdOn": "2026-05-07T12:00:00.000Z",
      "employeeId": 1,
      "employeeType": "string",
      "hours": 1,
      "id": 1,
      "invoiceId": 1,
      "memo": "string",
      "modifiedOn": "2026-05-07T12:00:00.000Z",
      "postedOn": "2026-05-07T12:00:00.000Z",
      "quantity": 1,
      "rate": 1,
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `active` | boolean |  |
| `activityCodeId` | number |  |
| `amount` | number |  |
| `businessUnitId` | number |  |
| `createdOn` | date |  |
| `employeeId` | number |  |
| `employeeType` | string |  |
| `hours` | number |  |
| `id` | number |  |
| `invoiceId` | number |  |
| `memo` | string |  |
| `modifiedOn` | date |  |
| `postedOn` | date |  |
| `quantity` | number |  |
| `rate` | number |  |
| `type` | string |  |

## Native endpoint

Through the native ServiceTitan API, this operation is `GET payroll/v2/tenant/{{credentials.tenant}}/payroll-adjustments` (base URL `https://{{credentials.baseUrl}}/`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/get-payroll-adjustments.md) for the provider-specific parameters and requirements.

