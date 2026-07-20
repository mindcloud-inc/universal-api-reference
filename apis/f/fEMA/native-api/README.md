# FEMA: Native API Reference

A consolidated summary of FEMA's API configuration and 40 documented operations, with links to official documentation.

- **Official docs:** https://www.fema.gov/about/openfema/api
- **OpenAPI specification:** https://www.fema.gov/api/open/metadata/v3.0/OpenApi.json
- **API base URL:** `https://www.fema.gov/api/open`

## Authentication

### No authentication

OpenFEMA public API access does not require provider credentials.

This API does not require request authentication.

[Official authentication documentation](https://www.fema.gov/about/openfema/api)

## API conventions

Responses from this API use JSON.

## Pagination

Use `$top` in the query string to set the page size (default 100; accepted range 1–10000). Use `$skip` in the query string as the record offset; numbering starts at 0.

## Filtering

Send filters in the query string. Supported operators: `eq`.

## Sorting

Set the sort field with `$orderby` in the query string. Use `ascending` for ascending order and `desc` for descending order. Only one sort field is accepted.

## Retry behavior

Retry responses with status codes `408,429,500,502,503,504`. Wait 1000 ms before the first retry. Stop after 3 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (40 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [List Declaration Denials](actions/list-declaration-denials.md) | `GET /v1/DeclarationDenials` | [docs](https://www.fema.gov/openfema-data-page/declaration-denials-v1) |
| [List Disaster Declarations Summaries](actions/list-disaster-declarations-summaries.md) | `GET /v2/DisasterDeclarationsSummaries` | [docs](https://www.fema.gov/openfema-data-page/Disaster-Declarations-Summaries-v2) |
| [List Emergency Management Performance Grants](actions/list-emergency-management-performance-grants.md) | `GET /v2/EmergencyManagementPerformanceGrants` | [docs](https://www.fema.gov/openfema-data-page/emergency-management-performance-grants-v2) |
| [List FEMA Regions](actions/list-fema-regions.md) | `GET /v2/FemaRegions` | [docs](https://www.fema.gov/openfema-data-page/fema-regions-v2) |
| [List FEMA Web Declaration Areas](actions/list-fema-web-declaration-areas.md) | `GET /v1/FemaWebDeclarationAreas` | [docs](https://www.fema.gov/openfema-data-page/fema-web-declaration-areas-v1) |
| [List FEMA Web Disaster Declarations](actions/list-fema-web-disaster-declarations.md) | `GET /v1/FemaWebDisasterDeclarations` | [docs](https://www.fema.gov/openfema-data-page/fema-web-disaster-declarations-v1) |
| [List FEMA Web Disaster Summaries](actions/list-fema-web-disaster-summaries.md) | `GET /v1/FemaWebDisasterSummaries` | [docs](https://www.fema.gov/openfema-data-page/fema-web-disaster-summaries-v1) |
| [List Hazard Mitigation Assistance Projects](actions/list-hazard-mitigation-assistance-projects.md) | `GET /v4/HazardMitigationAssistanceProjects` | [docs](https://www.fema.gov/openfema-data-page/hazard-mitigation-assistance-projects-v4) |
| [List Hazard Mitigation Plan Statuses](actions/list-hazard-mitigation-plan-statuses.md) | `GET /v1/HazardMitigationPlanStatuses` | [docs](https://www.fema.gov/openfema-data-page/hazard-mitigation-plan-statuses-v1) |
| [List HMA Mitigated Properties](actions/list-hma-mitigated-properties.md) | `GET /v4/HazardMitigationAssistanceMitigatedProperties` | [docs](https://www.fema.gov/openfema-data-page/hazard-mitigation-assistance-mitigated-properties-v4) |
| [List HMA Project Financial Transactions](actions/list-hma-project-financial-transactions.md) | `GET /v1/HazardMitigationAssistanceProjectsFinancialTransactions` | [docs](https://www.fema.gov/openfema-data-page/hazard-mitigation-assistance-projects-financial-transactions-v1) |
| [List HMA Subapplication Financial Transactions](actions/list-hma-subapplication-financial-transactions.md) | `GET /v1/HmaSubapplicationsFinancialTransactions` | [docs](https://www.fema.gov/openfema-data-page/HMA-Subapplications-Financial-Transactions-v1) |
| [List HMA Subapplications](actions/list-hma-subapplications.md) | `GET /v2/HmaSubapplications` | [docs](https://www.fema.gov/openfema-data-page/HMA-Subapplications-v2) |
| [List HMA Subapplications by NFIP CRS Communities](actions/list-hma-subapplications-by-nfip-crs-communities.md) | `GET /v1/HmaSubapplicationsByNfipCrsCommunities` | [docs](https://www.fema.gov/openfema-data-page/hma-subapplications-nfip-crs-communities-v1) |
| [List HMGP Disaster Summaries](actions/list-hmgp-disaster-summaries.md) | `GET /v2/HazardMitigationGrantProgramDisasterSummaries` | [docs](https://www.fema.gov/openfema-data-page/hazard-mitigation-grant-program-disaster-summaries-v2) |
| [List Housing Assistance Owners](actions/list-housing-assistance-owners.md) | `GET /v2/HousingAssistanceOwners` | [docs](https://www.fema.gov/openfema-data-page/housing-assistance-program-data-owners-v2) |
| [List Housing Assistance Renters](actions/list-housing-assistance-renters.md) | `GET /v2/HousingAssistanceRenters` | [docs](https://www.fema.gov/openfema-data-page/housing-assistance-program-data-renters-v2) |
| [List IHP Valid Registrations](actions/list-ihp-valid-registrations.md) | `GET /v2/IndividualsAndHouseholdsProgramValidRegistrations` | [docs](https://www.fema.gov/openfema-data-page/individuals-and-households-program-valid-registrations-v2) |
| [List Individual Assistance Housing Registrants](actions/list-individual-assistance-housing-registrants.md) | `GET /v1/IndividualAssistanceHousingRegistrantsLargeDisasters` | [docs](https://www.fema.gov/openfema-data-page/individual-assistance-housing-registrants-large-disasters-v1) |
| [List IPAWS Archived Alerts](actions/list-ipaws-archived-alerts.md) | `GET /v1/IpawsArchivedAlerts` | [docs](https://www.fema.gov/openfema-data-page/ipaws-archived-alerts-v1) |
| [List Mission Assignments](actions/list-mission-assignments.md) | `GET /v2/MissionAssignments` | [docs](https://www.fema.gov/openfema-data-page/mission-assignments-v2) |
| [List Multiple Loss Flood Properties](actions/list-multiple-loss-flood-properties.md) | `GET /v1/IndividualAssistanceMultipleLossFloodProperties` | [docs](https://www.fema.gov/openfema-data-page/Individual-Assistance-Multiple-Loss-Flood-Properties-v1) |
| [List NFIP Claims](actions/list-nfip-claims.md) | `GET /v2/FimaNfipClaims` | [docs](https://www.fema.gov/openfema-data-page/fima-nfip-redacted-claims-v2) |
| [List NFIP Community Layer Comprehensive](actions/list-nfip-community-layer-comprehensive.md) | `GET /v1/NfipCommunityLayerComprehensive` | [docs](https://www.fema.gov/openfema-data-page/nfip-community-layer-comprehensive-v1) |
| [List NFIP Community Status Book](actions/list-nfip-community-status-book.md) | `GET /v1/NfipCommunityStatusBook` | [docs](https://www.fema.gov/openfema-data-page/nfip-community-status-book-v1) |
| [List NFIP Multiple Loss Properties](actions/list-nfip-multiple-loss-properties.md) | `GET /v1/NfipMultipleLossProperties` | [docs](https://www.fema.gov/openfema-data-page/NFIP-Multiple-Loss-Properties-v1) |
| [List NFIP Policies](actions/list-nfip-policies.md) | `GET /v2/FimaNfipPolicies` | [docs](https://www.fema.gov/openfema-data-page/fima-nfip-redacted-policies-v2) |
| [List NFIP Residential Penetration Rates](actions/list-nfip-residential-penetration-rates.md) | `GET /v1/NfipResidentialPenetrationRates` | [docs](https://www.fema.gov/openfema-data-page/nfip-residential-penetration-rates-v1) |
| [List Non-Disaster Firefighter Grants](actions/list-non-disaster-firefighter-grants.md) | `GET /v1/NonDisasterAssistanceFirefighterGrants` | [docs](https://www.fema.gov/openfema-data-page/non-disaster-and-assistance-firefighter-grants-v1) |
| [List OpenFEMA Data Set Fields](actions/list-openfema-data-set-fields.md) | `GET /v1/DataSetFields` | [docs](https://www.fema.gov/openfema-data-page/openfema-data-set-fields-v1) |
| [List OpenFEMA Data Sets](actions/list-openfema-data-sets.md) | `GET /v1/DataSets` | [docs](https://www.fema.gov/openfema-data-page/openfema-data-sets-v1) |
| [List Public Assistance Applicants](actions/list-public-assistance-applicants.md) | `GET /v1/PublicAssistanceApplicants` | [docs](https://www.fema.gov/openfema-data-page/public-assistance-applicants-v1) |
| [List Public Assistance Funded Project Details](actions/list-public-assistance-funded-project-details.md) | `GET /v2/PublicAssistanceFundedProjectsDetails` | [docs](https://www.fema.gov/openfema-data-page/public-assistance-funded-projects-details-v2) |
| [List Public Assistance Funded Project Summaries](actions/list-public-assistance-funded-project-summaries.md) | `GET /v1/PublicAssistanceFundedProjectsSummaries` | [docs](https://www.fema.gov/openfema-data-page/public-assistance-funded-projects-summaries-v1) |
| [List Public Assistance Grant Award Activities](actions/list-public-assistance-grant-award-activities.md) | `GET /v2/PublicAssistanceGrantAwardActivities` | [docs](https://www.fema.gov/openfema-data-page/public-assistance-grant-award-activities-v2) |
| [List Public Assistance Program Deliveries](actions/list-public-assistance-program-deliveries.md) | `GET /v1/PublicAssistanceApplicantsProgramDeliveries` | [docs](https://www.fema.gov/openfema-data-page/public-assistance-applicants-program-deliveries-v1) |
| [List Public Assistance Second Appeals](actions/list-public-assistance-second-appeals.md) | `GET /v1/PublicAssistanceSecondAppealsTracker` | [docs](https://www.fema.gov/openfema-data-page/public-assistance-second-appeals-tracker-v1) |
| [List Registration Intake IHP Records](actions/list-registration-intake-ihp-records.md) | `GET /v2/RegistrationIntakeIndividualsHouseholdPrograms` | [docs](https://www.fema.gov/openfema-data-page/registration-intake-and-individuals-household-program-v2) |
| [List Training Class Schedule](actions/list-training-class-schedule.md) | `GET /v1/TrainingClassSchedule` | [docs](https://www.fema.gov/openfema-data-page/training-class-schedule-v1) |
| [List Training Course Catalog](actions/list-training-course-catalog.md) | `GET /v1/TrainingCourseCatalog` | [docs](https://www.fema.gov/openfema-data-page/training-course-catalog-v1) |
