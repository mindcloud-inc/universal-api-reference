# Search for Contacts with Apollo

Finds contacts in your Apollo account.

## Endpoint

- **Method:** `POST`
- **Path:** `v1/contacts/search`
- **Base URL:** `https://app.apollo.io/api`
- **Official documentation:** [Search for Contacts](https://docs.apollo.io/reference/search-for-contacts)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `label_ids[]` | query | `string<string>` | no | Send multiple values as a array. |
| `q_keywords` | query | `string` | no | Add keywords to narrow the search of the contacts in your team's Apollo account. Keywords can include combinations of names, job titles, employers (company names), and email addresses. Examples: `tim zheng`; `senior research analyst`; `microsoft` Send multiple values as a array separated by `;`. |
| `contact_stage_ids[]` | body | `array<string>` | no | The Apollo IDs for the contact stages that you want to include in your search results. If you add multiple contact stages, Apollo will include all contacts that match any of the stages, along with the other parameters, in the search results. Call the [List Contact Stages endpoint](https://docs.apollo.io/reference/list-contact-stages) to retrieve a list of all the contact stage IDs available in your Apollo account. Example: `6095a710bd01d100a506d4ae` |
| `contact_label_ids[]` | body | `array<string>` | no | The Apollo IDs for the labels that you want to include in your search results. If you add multiple labels, Apollo will include all contacts connected to any of the labels, along with the other parameters, in the search results. Example: `['6095a710bd01d100a506d4ae']` |
| `contact_stage_ids[]` | query | `list<string>` | no | The contact stages that you want to include in your search results. If you add multiple contact stages, Apollo will include all contacts that match any of the stages, along with the other parameters, in the search results. Send multiple values as a array separated by `&contact_stage_ids[]=`. |
| `sort_by_field` | body | `string` | no | Sort the matching contacts by 1 of the following options: - `contact_last_activity_date`: The most recent activity date recorded first. - `contact_email_last_opened_at`: The most recent email opened date first. - `contact_email_last_clicked_at`: The most recent email clicked first. - `contact_created_at`: The most recently created first. - `contact_updated_at`: The most recently updated first. |
| `sort_ascending` | body | `boolean` | no | Set to `true` to sort the matching contacts in ascending order. This parameter must be used with `sort_by_field`. Otherwise, the sorting logic is not applied. Example: `true` |
