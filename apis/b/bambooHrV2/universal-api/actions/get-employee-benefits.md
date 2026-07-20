# BambooHR: Get Employee Benefits

Retrieves employee benefit enrollments from BambooHR.

```
GET https://connect.mindcloud.co/v1/universal/bambooHrV2/latest/actions/get-employee-benefits
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a BambooHR `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bambooHrV2/latest/actions/get-employee-benefits?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/bambooHrV2/latest/actions/get-employee-benefits?${params}`, {
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
| `employeeIdFilter` | string | no | Filter employee benefits by BambooHR employee ID. Example: `4`. |
| `companyBenefitPlanIdFilter` | string | no | Filter employee benefits by BambooHR company benefit plan ID. Example: `35`. |
| `enrollmentStatusEffectiveDateFilter` | string | no | Filter employee benefits by enrollment status effective date. Example: `2026-01-01`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native BambooHR API returns.

## Native endpoint

Through the native BambooHR API, this operation is `GET /v1/benefit/employee_benefit` (base URL `https://mindcloud.bamboohr.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-employee-benefits.md) for the provider-specific parameters and requirements.

