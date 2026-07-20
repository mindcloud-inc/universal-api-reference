# Apollo: Search for Contacts

Finds contacts in your Apollo account.

```
GET https://connect.mindcloud.co/v1/universal/apolloio/latest/actions/search-for-contacts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Apollo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/apolloio/latest/actions/search-for-contacts?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/apolloio/latest/actions/search-for-contacts?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `labelIds` | string<string> | no | Accepts multiple values as an array. |
| `qKeywords` | string | no | Add keywords to narrow the search of the contacts in your team's Apollo account. Keywords can include combinations of names, job titles, employers (company names), and email addresses. Examples: `tim zheng`; `senior research analyst`; `microsoft` Accepts multiple values as an array. |
| `contactStageIds[]` | array<string> | no | The Apollo IDs for the contact stages that you want to include in your search results. If you add multiple contact stages, Apollo will include all contacts that match any of the stages, along with the other parameters, in the search results. Call the [List Contact Stages endpoint](https://docs.apollo.io/reference/list-contact-stages) to retrieve a list of all the contact stage IDs available in your Apollo account. Example: `6095a710bd01d100a506d4ae` |
| `contactLabelIds[]` | array<string> | no | The Apollo IDs for the labels that you want to include in your search results. If you add multiple labels, Apollo will include all contacts connected to any of the labels, along with the other parameters, in the search results. Example: `['6095a710bd01d100a506d4ae']` |
| `contactStage` | list<string> | no | The contact stages that you want to include in your search results. If you add multiple contact stages, Apollo will include all contacts that match any of the stages, along with the other parameters, in the search results. Accepts multiple values as an array. |
| `sortByField` | string | no | Sort the matching contacts by 1 of the following options: - `contact_last_activity_date`: The most recent activity date recorded first. - `contact_email_last_opened_at`: The most recent email opened date first. - `contact_email_last_clicked_at`: The most recent email clicked first. - `contact_created_at`: The most recently created first. - `contact_updated_at`: The most recently updated first. |
| `sortAscending` | boolean | no | Set to `true` to sort the matching contacts in ascending order. This parameter must be used with `sort_by_field`. Otherwise, the sorting logic is not applied. Example: `true` |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Apollo API returns.

## Native endpoint

Through the native Apollo API, this operation is `POST v1/contacts/search` (base URL `https://app.apollo.io/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-for-contacts.md) for the provider-specific parameters and requirements.

