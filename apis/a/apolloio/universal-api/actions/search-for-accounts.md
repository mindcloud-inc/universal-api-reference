# Apollo: Search for Accounts

Finds accounts in your Apollo account.

```
GET https://connect.mindcloud.co/v1/universal/apolloio/latest/actions/search-for-accounts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Apollo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/apolloio/latest/actions/search-for-accounts?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/apolloio/latest/actions/search-for-accounts?${params}`, {
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
| `qOrganizationName` | string | no | Add keywords to narrow the search of the accounts in your team's Apollo account. Keywords should directly match at least part of an account's name. For example, searching the keyword `marketing` might return the result `NY Marketing Unlimited`, but not `NY Market Analysts`. This parameter only searches account names, not other account fields. Examples: `apollo`; `microsoft`; `marketing` |
| `accountStageIds[]` | array<string> | no | The Apollo IDs for the account stages that you want to include in your search results. If you add multiple account stages, Apollo will include all accounts that match any of the stages, along with the other parameters, in the search results. Call the [List Account Stages endpoint](https://docs.apollo.io/reference/list-account-stages) to retrieve a list of all the account stage IDs available in your Apollo account. Example: `61b8e913e0f4d2012e3af74e` |
| `accountLabelIds[]` | array<string> | no | The Apollo IDs for the labels that you want to include in your search results. If you add multiple labels, Apollo will include all accounts connected to any of the labels, along with the other parameters, in the search results. Example: `['6095a710bd01d100a506d4ae']` |
| `sortByField` | string | no | Sort the matching accounts by 1 of the following options: - `account_last_activity_date`: The most recent activity date recorded first. - `account_created_at`: The most recently created first. - `account_updated_at`: The most recently updated first. |
| `sortAscending` | boolean | no | Set to `true` to sort the matching accounts in ascending order. This parameter must be used with `sort_by_field`. Otherwise, the sorting logic is not applied. Example: `true` |

## Response

```json
{
  "success": true,
  "data": [
    {
      "disableEuProspecting": true,
      "hasJoin": true,
      "numFetchResult": {},
      "pagination": {
        "page": 1,
        "perPage": 1,
        "totalEntries": 1,
        "totalPages": 1
      },
      "partialResultsLimit": 1,
      "partialResultsOnly": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `disableEuProspecting` | boolean |  |
| `hasJoin` | boolean |  |
| `numFetchResult` | object |  |
| `pagination.page` | number |  |
| `pagination.perPage` | number |  |
| `pagination.totalEntries` | number |  |
| `pagination.totalPages` | number |  |
| `partialResultsLimit` | number |  |
| `partialResultsOnly` | boolean |  |

## Native endpoint

Through the native Apollo API, this operation is `POST v1/accounts/search` (base URL `https://app.apollo.io/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-for-accounts.md) for the provider-specific parameters and requirements.

