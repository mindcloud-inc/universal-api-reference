# Doyle HCM: Universal API

Doyle HCM provides payroll and HR services for U.S. employers through white-label employer and employee payroll portals backed by Worklio.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/doyleHCM/latest
- **Actions:** 20
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://doylehcm.com
- **Vendor API docs:** https://apidocs.worklio.com/docs/how-to-get-api-access

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get current user](actions/get-current-user.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/doyleHCM/latest/actions/get-current-user?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (20)

### Companies

| Action | Method | Description |
| --- | --- | --- |
| [Get company](actions/get-company.md) | GET | Retrieves a company from Doyle HCM by ID. |
| [Get company KYC status](actions/get-company-kyc-status.md) | GET |  |
| [List companies](actions/list-companies.md) | GET | Retrieves visible companies from Doyle HCM. |

### Dashboards

| Action | Method | Description |
| --- | --- | --- |
| [Get company dashboard](actions/get-company-dashboard.md) | GET | Retrieves a company dashboard definition from Doyle HCM. |
| [Get dashboard](actions/get-dashboard.md) | GET | Retrieves the current admin dashboard definition from Doyle HCM. |

### Departments

| Action | Method | Description |
| --- | --- | --- |
| [Create company department](actions/create-company-department.md) | POST | Creates a company department in Doyle HCM. |
| [Get company department](actions/get-company-department.md) | GET | Retrieves a company department from Doyle HCM. |
| [List company departments](actions/list-company-departments.md) | GET | Retrieves company departments from Doyle HCM. |
| [Update company department](actions/update-company-department.md) | PUT | Updates a company department in Doyle HCM. |

### Documents

| Action | Method | Description |
| --- | --- | --- |
| [Get company KYC document type](actions/get-company-kyc-document-type.md) | GET | Retrieves a company KYC document type from Doyle HCM. |
| [List company KYC document types](actions/list-company-kyc-document-types.md) | GET | Retrieves company KYC document types from Doyle HCM. |

### Locations

| Action | Method | Description |
| --- | --- | --- |
| [Get company work location](actions/get-company-work-location.md) | GET | Retrieves a company work location from Doyle HCM. |
| [List company work locations](actions/list-company-work-locations.md) | GET | Retrieves company work locations from Doyle HCM. |

### Policies

| Action | Method | Description |
| --- | --- | --- |
| [Get company access policy](actions/get-company-access-policy.md) | GET | Retrieves the company access policy from Doyle HCM. |
| [Set company access policy](actions/set-company-access-policy.md) | PUT | Updates the company access policy in Doyle HCM. |

### Positions

| Action | Method | Description |
| --- | --- | --- |
| [Create company position](actions/create-company-position.md) | POST | Creates a company position in Doyle HCM. |
| [List company positions](actions/list-company-positions.md) | GET | Retrieves company positions from Doyle HCM. |
| [Update company position](actions/update-company-position.md) | PUT | Updates a company position in Doyle HCM. |

### Users

| Action | Method | Description |
| --- | --- | --- |
| [Get current user](actions/get-current-user.md) | GET | Retrieves the current user profile from Doyle HCM. |
| [List company signatories](actions/list-company-signatories.md) | GET | Retrieves company signatories from Doyle HCM. |

