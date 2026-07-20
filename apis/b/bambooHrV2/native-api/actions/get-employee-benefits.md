# Get Employee Benefits with BambooHR

Retrieves employee benefit enrollments from BambooHR.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/benefit/employee_benefit`
- **Base URL:** `https://mindcloud.bamboohr.com/api`
- **Official documentation:** [Get Employee Benefits](https://documentation.bamboohr.com/reference/get-employee-benefit-1)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `filters.employeeId` | body | `string` | no | Filter employee benefits by BambooHR employee ID. |
| `filters.companyBenefitPlanId` | body | `string` | no | Filter employee benefits by BambooHR company benefit plan ID. |
| `filters.enrollmentStatusEffectiveDate` | body | `string` | no | Filter employee benefits by enrollment status effective date. |
