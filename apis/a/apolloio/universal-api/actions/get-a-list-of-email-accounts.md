# Apollo: Get Inboxes

Retrieves information about the linked email inboxes that users (your teammates) use under the authenticated account. This endpoint returns IDs for each of your team's linked email accounts, which can be used with the "Add Contacts to a Sequence" action.

```
GET https://connect.mindcloud.co/v1/universal/apolloio/latest/actions/get-a-list-of-email-accounts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Apollo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/apolloio/latest/actions/get-a-list-of-email-accounts?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/apolloio/latest/actions/get-a-list-of-email-accounts?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Apollo API returns.

## Native endpoint

Through the native Apollo API, this operation is `GET v1/email_accounts` (base URL `https://app.apollo.io/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-a-list-of-email-accounts.md) for the provider-specific parameters and requirements.

