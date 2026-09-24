# <img src="https://images.mindcloud.co/apps/icons/image-2848-vectorized_1782233120520.png" alt="ADP logo" width="28" height="28"> ADP: Universal API

Experience better HR and payroll

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/adp/latest
- **Category:** Human Resources / HRIS
- **Actions:** 17
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.adp.com/
- **Vendor API docs:** https://developers.adp.com/build/api-explorer

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Business Units](actions/list-business-units.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/adp/latest/actions/list-business-units?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (17)

### Employees

| Action | Method | Description |
| --- | --- | --- |
| [Get Worker](actions/get-worker.md) | GET |  |
| [List Workers](actions/get-workers.md) | GET | Request the list of all available workers. |

### Locations

| Action | Method | Description |
| --- | --- | --- |
| [List Associate Work Locations](actions/list-associate-work-locations.md) | GET | Associate Work Locations |
| [List Business Units](actions/list-business-units.md) | GET | Associate Business Units |

### Other

| Action | Method | Description |
| --- | --- | --- |
| [List Pay Data Input](actions/list-pay-data-input.md) | GET |  |

### Pay Statement

| Action | Method | Description |
| --- | --- | --- |
| [Get Worker Pay Statement](actions/list-worker-pay-statement-by-uri.md) | GET |  |
| [List Worker Pay Statements](actions/list-worker-pay-statements.md) | GET |  |

### Payroll Group Pay Period

| Action | Method | Description |
| --- | --- | --- |
| [List Payroll Groups](actions/list-payroll-groups.md) | GET |  |

### Payroll Output

| Action | Method | Description |
| --- | --- | --- |
| [Get Payroll Earning Allocations](actions/get-payroll-earning-allocations.md) | GET |  |
| [List Payroll Outputs](actions/list-payroll-outputs.md) | GET |  |

### Payrolls

| Action | Method | Description |
| --- | --- | --- |
| [Create Payroll Batch](actions/create-payroll-batch.md) | POST |  |
| [Get Payroll Metadata](actions/get-payroll-meta-data.md) | GET |  |

### Time Off Balance

| Action | Method | Description |
| --- | --- | --- |
| [List Worker Time Off Balances](actions/list-worker-time-off-balances.md) | GET |  |

### Time Off Request

| Action | Method | Description |
| --- | --- | --- |
| [List Worker Time Off Requests](actions/list-worker-time-off-requests.md) | GET |  |

### Timesheets

| Action | Method | Description |
| --- | --- | --- |
| [Create Time Card](actions/create-time-card.md) | POST |  |
| [List Time Cards by Associate ID](actions/list-time-cards-by-associate-id.md) | GET | Getting all presence time entries for an employee and for a given period. |

### Worker Leave

| Action | Method | Description |
| --- | --- | --- |
| [List Worker Leaves](actions/list-worker-leaves.md) | GET |  |

