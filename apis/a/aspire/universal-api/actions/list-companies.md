# Aspire: List Companies

Retrieves a list of commercial or enterprise businesses associated with a contact.

```
GET https://connect.mindcloud.co/v1/universal/aspire/latest/actions/list-companies
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Aspire `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [filtering](../filtering.md) (`where`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/aspire/latest/actions/list-companies?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/aspire/latest/actions/list-companies?${params}`, {
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
      "active": true,
      "companyID": 1,
      "companyName": "Ava Chen",
      "createdByUserID": 1,
      "createdByUserName": "Ava Chen",
      "createdDateTime": "string",
      "deniedTimeEmail": {},
      "earliestOpportunityWonDate": "string",
      "modifiedByUserID": 1,
      "modifiedByUserName": "Ava Chen",
      "modifiedDateTime": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `active` | boolean |  |
| `companyID` | number |  |
| `companyName` | string |  |
| `createdByUserID` | number |  |
| `createdByUserName` | string |  |
| `createdDateTime` | string |  |
| `deniedTimeEmail` | object |  |
| `earliestOpportunityWonDate` | string |  |
| `modifiedByUserID` | number |  |
| `modifiedByUserName` | string |  |
| `modifiedDateTime` | string |  |

## Native endpoint

Through the native Aspire API, this operation is `GET Companies` (base URL `https://{{credentials.environment}}.youraspire.com/`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-companies.md) for the provider-specific parameters and requirements.

