# Aspire: List Activity Contacts

Retrieves activity contacts from your Aspire account.

```
GET https://connect.mindcloud.co/v1/universal/aspire/latest/actions/list-activity-contacts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Aspire `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [filtering](../filtering.md) (`where`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/aspire/latest/actions/list-activity-contacts?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/aspire/latest/actions/list-activity-contacts?${params}`, {
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
| `expand` | string | no |  |
| `filter` | string | no |  |
| `orderBy` | string | no |  |
| `select` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "ActivityContactID": 1,
      "ActivityID": 1,
      "AssignmentType": "string",
      "ContactID": 1,
      "ContactName": "Ava Chen",
      "EmailAddress": "ava@example.com",
      "IgnoreNullContact": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `ActivityContactID` | number |  |
| `ActivityID` | number |  |
| `AssignmentType` | string |  |
| `ContactID` | number |  |
| `ContactName` | string |  |
| `EmailAddress` | string |  |
| `IgnoreNullContact` | boolean |  |

## Native endpoint

Through the native Aspire API, this operation is `GET ActivityContacts` (base URL `https://{{credentials.environment}}.youraspire.com/`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-activity-contacts.md) for the provider-specific parameters and requirements.

