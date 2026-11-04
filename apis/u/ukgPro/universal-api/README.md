# <img src="https://images.mindcloud.co/apps/icons/ukg-pro-icon_1782394587940.jpg" alt="UKG Pro logo" width="28" height="28"> UKG Pro: Universal API

UKG Pro through the MindCloud Universal API.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/ukgPro/latest
- **Actions:** 13
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.ukg.com/
- **Vendor API docs:** https://developer.ukg.com/hcm/reference/welcome-to-the-pro-developer-hub

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Platform Configuration Fields](actions/get-platform-configuration-fields.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ukgPro/latest/actions/get-platform-configuration-fields?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (13)

### Companies

| Action | Method | Description |
| --- | --- | --- |
| [Get Platform Configuration Fields](actions/get-platform-configuration-fields.md) | GET |  |

### Employees

| Action | Method | Description |
| --- | --- | --- |
| [Get All Org Levels](actions/get-all-org-levels.md) | GET |  |
| [Get Employee Changes](actions/get-employee-changes.md) | GET |  |
| [Get Employee Demographic Details](actions/get-employee-demographic-details.md) | GET |  |
| [Get Employment Details](actions/get-employment-details.md) | GET |  |
| [Get Person Details](actions/get-person-details.md) | GET |  |
| [Retrieve All Job Configurations](actions/retrieve-all-job-configurations.md) | GET |  |
| [Retrieve All Locations Configurations](actions/retrieve-all-locations-configurations.md) | GET |  |

### Other

| Action | Method | Description |
| --- | --- | --- |
| [Get All Employee Job History Details](actions/get-all-employee-job-history-details.md) | GET |  |
| [Get Earnings History Base Elements](actions/get-earnings-history-base-elements.md) | GET | Payroll earnings history base elements for one pay date (page / per_Page). |
| [Get Employee Employment Details](actions/get-employee-employment-details.md) | GET |  |
| [Get Employee Multiple Phone Numbers](actions/get-employee-multiple-phone-numbers.md) | GET |  |
| [Get User Defined Fields](actions/get-user-defined-fields.md) | GET |  |

