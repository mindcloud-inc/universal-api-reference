# Flat Advanced Search with LeadIQ

## Endpoint

- **Method:** `POST`
- **Path:** `graphql`
- **Base URL:** `https://api.leadiq.com/`
- **Official documentation:** [Flat Advanced Search](https://developer.leadiq.com/#query-flatAdvancedSearch)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `variables.input.companyFilter` | body | `object` | no | CompanyFilter object. Common keys include domains, names, linkedinIds, industries, sizes, locations, and revenue filters. |
| `variables.input.contactFilter` | body | `object` | no | ContactFilter object. Common keys include names, titles, linkedinIds, seniorities, roles, locations, updatedAt, newHireFrom, and newPromotionFrom. |
| `variables.input.limit` | body | `number` | no | Maximum number of contacts to return. |
| `variables.input.companyExcludedFilter` | body | `object` | no | Optional CompanyFilter object for companies to exclude from the search. |
| `variables.input.contactExcludedFilter` | body | `object` | no | Optional ContactFilter object for contacts to exclude from the search. |
| `variables.input.sortContactsBy[]` | body | `array<string>` | no | Optional array of contact sort values such as UpdatedAtDesc, NameAsc, RoleAsc, or SeniorityDesc. |
| `variables.input.skip` | body | `number` | no | Number of matching contacts to skip before returning results. |
