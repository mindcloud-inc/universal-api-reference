# FEMA Universal API Filtering

Filterable list actions accept a `where` query parameter written as an RSQL expression. MindCloud translates it into the filtering format FEMA expects, and each action page lists the fields available to filter.

| Operator | Meaning | Example |
| --- | --- | --- |
| `==` / `!=` | Equals / does not equal | `status==active` |
| `>` / `>=` / `<` / `<=` | Comparisons | `createdAt>=2026-01-01` |
| `=like=` | Contains text, with `*` wildcards | `name=like=*dan*` |

Combine conditions with `;` for AND and `,` for OR. For example, `where=status==active;createdAt>=2026-01-01` returns active records created in 2026 or later.

## FEMA actions that support filtering

- [List Declaration Denials](actions/list-declaration-denials.md)
- [List Disaster Declarations Summaries](actions/list-disaster-declarations-summaries.md)
- [List Emergency Management Performance Grants](actions/list-emergency-management-performance-grants.md)
- [List FEMA Regions](actions/list-fema-regions.md)
- [List FEMA Web Declaration Areas](actions/list-fema-web-declaration-areas.md)
- [List FEMA Web Disaster Declarations](actions/list-fema-web-disaster-declarations.md)
- [List FEMA Web Disaster Summaries](actions/list-fema-web-disaster-summaries.md)
- [List Hazard Mitigation Assistance Projects](actions/list-hazard-mitigation-assistance-projects.md)
- [List Hazard Mitigation Plan Statuses](actions/list-hazard-mitigation-plan-statuses.md)
- [List HMA Mitigated Properties](actions/list-hma-mitigated-properties.md)
- [List HMA Project Financial Transactions](actions/list-hma-project-financial-transactions.md)
- [List HMA Subapplication Financial Transactions](actions/list-hma-subapplication-financial-transactions.md)
- [List HMA Subapplications](actions/list-hma-subapplications.md)
- [List HMA Subapplications by NFIP CRS Communities](actions/list-hma-subapplications-by-nfip-crs-communities.md)
- [List HMGP Disaster Summaries](actions/list-hmgp-disaster-summaries.md)
- [List Housing Assistance Owners](actions/list-housing-assistance-owners.md)
- [List Housing Assistance Renters](actions/list-housing-assistance-renters.md)
- [List IHP Valid Registrations](actions/list-ihp-valid-registrations.md)
- [List Individual Assistance Housing Registrants](actions/list-individual-assistance-housing-registrants.md)
- [List IPAWS Archived Alerts](actions/list-ipaws-archived-alerts.md)
- [List Mission Assignments](actions/list-mission-assignments.md)
- [List Multiple Loss Flood Properties](actions/list-multiple-loss-flood-properties.md)
- [List NFIP Claims](actions/list-nfip-claims.md)
- [List NFIP Community Layer Comprehensive](actions/list-nfip-community-layer-comprehensive.md)
- [List NFIP Community Status Book](actions/list-nfip-community-status-book.md)
- [List NFIP Multiple Loss Properties](actions/list-nfip-multiple-loss-properties.md)
- [List NFIP Policies](actions/list-nfip-policies.md)
- [List NFIP Residential Penetration Rates](actions/list-nfip-residential-penetration-rates.md)
- [List Non-Disaster Firefighter Grants](actions/list-non-disaster-firefighter-grants.md)
- [List OpenFEMA Data Set Fields](actions/list-openfema-data-set-fields.md)
- [List OpenFEMA Data Sets](actions/list-openfema-data-sets.md)
- [List Public Assistance Applicants](actions/list-public-assistance-applicants.md)
- [List Public Assistance Funded Project Details](actions/list-public-assistance-funded-project-details.md)
- [List Public Assistance Funded Project Summaries](actions/list-public-assistance-funded-project-summaries.md)
- [List Public Assistance Grant Award Activities](actions/list-public-assistance-grant-award-activities.md)
- [List Public Assistance Program Deliveries](actions/list-public-assistance-program-deliveries.md)
- [List Public Assistance Second Appeals](actions/list-public-assistance-second-appeals.md)
- [List Registration Intake IHP Records](actions/list-registration-intake-ihp-records.md)
- [List Training Class Schedule](actions/list-training-class-schedule.md)
- [List Training Course Catalog](actions/list-training-course-catalog.md)
