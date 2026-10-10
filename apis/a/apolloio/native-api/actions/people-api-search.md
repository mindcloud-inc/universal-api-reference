# People API Search with Apollo

## Endpoint

- **Method:** `POST`
- **Path:** `v1/mixed_people/api_search`
- **Base URL:** `https://app.apollo.io/api`
- **Official documentation:** [People API Search](https://docs.apollo.io/reference/people-api-search)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `person_titles[]` | query | `array<string>` | no | — |
| `include_similar_titles` | query | `boolean` | no | — |
| `organization_ids[]` | query | `array<string>` | no | — |
| `q_organization_domains_list[]` | query | `array<string>` | no | — |
| `person_seniorities` | query | `list<string>` | no | Accepted values: `c_suite`, `director`, `entry`, `founder`, `head`, `intern`, `manager`, `owner`, `partner`, `senior`, `vp`. Send multiple values as a array. |
| `person_locations[]` | query | `array<string>` | no | — |
| `organization_locations[]` | query | `array<string>` | no | — |
| `organization_num_employees_ranges[]` | query | `array<string>` | no | — |
| `contact_email_status` | query | `list<string>` | no | Accepted values: `likely to engage`, `unavailable`, `unverified`, `verified`. Send multiple values as a array. |
| `q_person_name` | query | `string` | no | — |
| `currently_using_any_of_technology_uids[]` | query | `array<string>` | no | — |
| `not_organization_websites_list[]` | query | `array<string>` | no | — |
