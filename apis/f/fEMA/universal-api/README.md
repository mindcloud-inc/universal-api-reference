# <img src="https://images.mindcloud.co/apps/icons/id-px3kb-q0j-1777483008641_1777483062326.jpeg" alt="FEMA logo" width="28" height="28"> FEMA: Universal API

Access FEMA disaster, assistance, mitigation, and grant data

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/fEMA/latest
- **Category:** Business Intelligence / Data Extraction
- **Actions:** 40
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.fema.gov/about/reports-and-data/openfema
- **Vendor API docs:** https://www.fema.gov/about/openfema/api

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Disaster Declarations Summaries](actions/list-disaster-declarations-summaries.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/fEMA/latest/actions/list-disaster-declarations-summaries?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (40)

### Declaration Denial

| Action | Method | Description |
| --- | --- | --- |
| [List Declaration Denials](actions/list-declaration-denials.md) | GET | Retrieves declaration denials from FEMA. |

### Disaster Declaration Summary

| Action | Method | Description |
| --- | --- | --- |
| [List Disaster Declarations Summaries](actions/list-disaster-declarations-summaries.md) | GET | Retrieves disaster declaration summaries from FEMA. |

### Emergency Management Performance Grant

| Action | Method | Description |
| --- | --- | --- |
| [List Emergency Management Performance Grants](actions/list-emergency-management-performance-grants.md) | GET | Retrieves emergency management performance grants from FEMA. |

### Fema Region

| Action | Method | Description |
| --- | --- | --- |
| [List FEMA Regions](actions/list-fema-regions.md) | GET | Retrieves FEMA regions. |

### Fema Web Declaration Area

| Action | Method | Description |
| --- | --- | --- |
| [List FEMA Web Declaration Areas](actions/list-fema-web-declaration-areas.md) | GET | Retrieves FEMA web declaration areas. |

### Fema Web Disaster Declaration

| Action | Method | Description |
| --- | --- | --- |
| [List FEMA Web Disaster Declarations](actions/list-fema-web-disaster-declarations.md) | GET | Retrieves FEMA web disaster declarations. |

### Fema Web Disaster Summary

| Action | Method | Description |
| --- | --- | --- |
| [List FEMA Web Disaster Summaries](actions/list-fema-web-disaster-summaries.md) | GET | Retrieves FEMA web disaster summaries. |

### Hazard Mitigation Assistance Project

| Action | Method | Description |
| --- | --- | --- |
| [List Hazard Mitigation Assistance Projects](actions/list-hazard-mitigation-assistance-projects.md) | GET | Retrieves hazard mitigation assistance projects from FEMA. |

### Hazard Mitigation Plan Status

| Action | Method | Description |
| --- | --- | --- |
| [List Hazard Mitigation Plan Statuses](actions/list-hazard-mitigation-plan-statuses.md) | GET | Retrieves hazard mitigation plan statuses from FEMA. |

### Hma Mitigated Property

| Action | Method | Description |
| --- | --- | --- |
| [List HMA Mitigated Properties](actions/list-hma-mitigated-properties.md) | GET | Retrieves HMA mitigated properties from FEMA. |

### Hma Project Financial Transaction

| Action | Method | Description |
| --- | --- | --- |
| [List HMA Project Financial Transactions](actions/list-hma-project-financial-transactions.md) | GET | Retrieves HMA project financial transactions from FEMA. |

### Hma Subapplication

| Action | Method | Description |
| --- | --- | --- |
| [List HMA Subapplications](actions/list-hma-subapplications.md) | GET | Retrieves HMA subapplications from FEMA. |

### Hma Subapplication Financial Transaction

| Action | Method | Description |
| --- | --- | --- |
| [List HMA Subapplication Financial Transactions](actions/list-hma-subapplication-financial-transactions.md) | GET | Retrieves HMA subapplication financial transactions from FEMA. |

### Hma Subapplication Nfip Crs Community

| Action | Method | Description |
| --- | --- | --- |
| [List HMA Subapplications by NFIP CRS Communities](actions/list-hma-subapplications-by-nfip-crs-communities.md) | GET | Retrieves HMA subapplications for NFIP CRS communities. |

### Hmgp Disaster Summary

| Action | Method | Description |
| --- | --- | --- |
| [List HMGP Disaster Summaries](actions/list-hmgp-disaster-summaries.md) | GET | Retrieves HMGP disaster summaries from FEMA. |

### Housing Assistance Owner Record

| Action | Method | Description |
| --- | --- | --- |
| [List Housing Assistance Owners](actions/list-housing-assistance-owners.md) | GET | Retrieves housing assistance owner records from FEMA. |

### Housing Assistance Renter Record

| Action | Method | Description |
| --- | --- | --- |
| [List Housing Assistance Renters](actions/list-housing-assistance-renters.md) | GET | Retrieves housing assistance renter records from FEMA. |

### Ihp Valid Registration

| Action | Method | Description |
| --- | --- | --- |
| [List IHP Valid Registrations](actions/list-ihp-valid-registrations.md) | GET | Retrieves IHP valid registrations from FEMA. |

### Individual Assistance Housing Registrant

| Action | Method | Description |
| --- | --- | --- |
| [List Individual Assistance Housing Registrants](actions/list-individual-assistance-housing-registrants.md) | GET | Retrieves individual assistance housing registrants from FEMA. |

### Ipaws Archived Alert

| Action | Method | Description |
| --- | --- | --- |
| [List IPAWS Archived Alerts](actions/list-ipaws-archived-alerts.md) | GET | Retrieves IPAWS archived alerts from FEMA. |

### Mission Assignment

| Action | Method | Description |
| --- | --- | --- |
| [List Mission Assignments](actions/list-mission-assignments.md) | GET | Retrieves mission assignments from FEMA. |

### Multiple Loss Flood Property

| Action | Method | Description |
| --- | --- | --- |
| [List Multiple Loss Flood Properties](actions/list-multiple-loss-flood-properties.md) | GET | Retrieves multiple loss flood properties from FEMA. |

### Nfip Claim

| Action | Method | Description |
| --- | --- | --- |
| [List NFIP Claims](actions/list-nfip-claims.md) | GET | Retrieves NFIP claims from FEMA. |

### Nfip Community Layer Comprehensive Record

| Action | Method | Description |
| --- | --- | --- |
| [List NFIP Community Layer Comprehensive](actions/list-nfip-community-layer-comprehensive.md) | GET | Retrieves NFIP community layer records from FEMA. |

### Nfip Community Status Book Entry

| Action | Method | Description |
| --- | --- | --- |
| [List NFIP Community Status Book](actions/list-nfip-community-status-book.md) | GET | Retrieves the NFIP Community Status Book from FEMA. |

### Nfip Multiple Loss Property

| Action | Method | Description |
| --- | --- | --- |
| [List NFIP Multiple Loss Properties](actions/list-nfip-multiple-loss-properties.md) | GET | Retrieves NFIP multiple loss properties from FEMA. |

### Nfip Policy

| Action | Method | Description |
| --- | --- | --- |
| [List NFIP Policies](actions/list-nfip-policies.md) | GET | Retrieves NFIP policies from FEMA. |

### Nfip Residential Penetration Rate

| Action | Method | Description |
| --- | --- | --- |
| [List NFIP Residential Penetration Rates](actions/list-nfip-residential-penetration-rates.md) | GET | Retrieves NFIP residential penetration rates from FEMA. |

### Non-disaster Firefighter Grant

| Action | Method | Description |
| --- | --- | --- |
| [List Non-Disaster Firefighter Grants](actions/list-non-disaster-firefighter-grants.md) | GET | Retrieves non-disaster firefighter grants from FEMA. |

### Openfema Data Set

| Action | Method | Description |
| --- | --- | --- |
| [List OpenFEMA Data Sets](actions/list-openfema-data-sets.md) | GET | Retrieves OpenFEMA data sets from FEMA. |

### Openfema Data Set Field

| Action | Method | Description |
| --- | --- | --- |
| [List OpenFEMA Data Set Fields](actions/list-openfema-data-set-fields.md) | GET | Retrieves OpenFEMA data set fields from FEMA. |

### Public Assistance Applicant

| Action | Method | Description |
| --- | --- | --- |
| [List Public Assistance Applicants](actions/list-public-assistance-applicants.md) | GET | Retrieves public assistance applicants from FEMA. |

### Public Assistance Funded Project Detail

| Action | Method | Description |
| --- | --- | --- |
| [List Public Assistance Funded Project Details](actions/list-public-assistance-funded-project-details.md) | GET | Retrieves public assistance funded project details from FEMA. |

### Public Assistance Funded Project Summary

| Action | Method | Description |
| --- | --- | --- |
| [List Public Assistance Funded Project Summaries](actions/list-public-assistance-funded-project-summaries.md) | GET | Retrieves public assistance funded project summaries from FEMA. |

### Public Assistance Grant Award Activity

| Action | Method | Description |
| --- | --- | --- |
| [List Public Assistance Grant Award Activities](actions/list-public-assistance-grant-award-activities.md) | GET | Retrieves public assistance grant award activities from FEMA. |

### Public Assistance Program Delivery

| Action | Method | Description |
| --- | --- | --- |
| [List Public Assistance Program Deliveries](actions/list-public-assistance-program-deliveries.md) | GET | Retrieves public assistance program deliveries from FEMA. |

### Public Assistance Second Appeal

| Action | Method | Description |
| --- | --- | --- |
| [List Public Assistance Second Appeals](actions/list-public-assistance-second-appeals.md) | GET | Retrieves public assistance second appeals from FEMA. |

### Registration Intake Ihp Record

| Action | Method | Description |
| --- | --- | --- |
| [List Registration Intake IHP Records](actions/list-registration-intake-ihp-records.md) | GET | Retrieves registration intake IHP records from FEMA. |

### Training Class Schedule

| Action | Method | Description |
| --- | --- | --- |
| [List Training Class Schedule](actions/list-training-class-schedule.md) | GET | Retrieves the FEMA training class schedule. |

### Training Course Catalog Entry

| Action | Method | Description |
| --- | --- | --- |
| [List Training Course Catalog](actions/list-training-course-catalog.md) | GET | Retrieves FEMA training course catalog entries. |

