# <img src="https://images.mindcloud.co/apps/icons/idqh-rbyu-qg-logos_1777308828784.jpeg" alt="Ruly logo" width="28" height="28"> Ruly: Universal API

Ruly: Build apps, automate workflows, and manage data

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/ruly/latest
- **Category:** IT Operations / Database
- **Actions:** 9
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://rulyapp.com/
- **Vendor API docs:** https://rulyapp.com/quick-tips-using-ruly-api-in-postman-video/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Employees](actions/list-employees.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ruly/latest/actions/list-employees?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (9)

### Employees

| Action | Method | Description |
| --- | --- | --- |
| [Create Employee Record](actions/create-employee-record.md) | POST |  |
| [Delete Employee Record](actions/delete-employee-record.md) | DELETE |  |
| [Get Employee](actions/get-employee.md) | GET |  |
| [Get Employee Records with Specific Fields](actions/get-employee-records-with-specific-fields.md) | GET |  |
| [Get Filtered Employee Records](actions/get-filtered-employee-records.md) | GET |  |
| [Get Linked Records from Employee](actions/get-linked-records-from-employee.md) | GET |  |
| [List Employees](actions/list-employees.md) | GET |  |
| [List Employees Sorted by Last Name](actions/list-employees-sorted-by-last-name.md) | GET |  |
| [Update Employee City](actions/update-employee-city.md) | PUT |  |

