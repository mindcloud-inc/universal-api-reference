# ActiveTrail: List Contacts

Retrieves a list of contacts from ActiveTrail.

```
GET https://connect.mindcloud.co/v1/universal/activeTrail/latest/actions/list-contacts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ActiveTrail `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/activeTrail/latest/actions/list-contacts?connectionId=$CONNECTION_ID&limit=25&offset=0&customerStates=ACTIVE" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "customerStates": "ACTIVE"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/activeTrail/latest/actions/list-contacts?${params}`, {
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
| `customerStates` | list<string> | yes | Choose the states of the contacts you want to get. One of: `ACTIVE`, `ALL`, `BOUNCED`, `CUSTOMER_REQUEST`, `INACTIVE`, `QUARANTINED`, `SPAM_COMPLIENT`. |
| `fromDate` | date | no | Only include contacts from this date forward. |
| `searchTerm` | string | no | Search contacts by a free-text term. |
| `toDate` | date | no | Only include contacts up to this date. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native ActiveTrail API returns.

## Native endpoint

Through the native ActiveTrail API, this operation is `GET /contacts` (base URL `https://webapi.mymarketing.co.il/api`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-contacts.md) for the provider-specific parameters and requirements.

