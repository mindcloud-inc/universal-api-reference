# Aspire: List Property Contacts



```
GET https://connect.mindcloud.co/v1/universal/aspire/latest/actions/list-property-contacts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Aspire `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [filtering](../filtering.md) (`where`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/aspire/latest/actions/list-property-contacts?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/aspire/latest/actions/list-property-contacts?${params}`, {
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
      "billingContact": true,
      "companyID": 1,
      "companyName": "Ava Chen",
      "contactID": 1,
      "contactName": "Ava Chen",
      "createdByUserID": 1,
      "createdByUserName": "Ava Chen",
      "createdDateTime": "string",
      "emailInvoiceContact": true,
      "emailNotificationsContact": true,
      "lastModifiedByUserID": {},
      "lastModifiedByUserName": {},
      "lastModifiedDateTime": {},
      "primaryContact": true,
      "propertyID": 1,
      "propertyName": "Ava Chen",
      "sMSNotificationsContact": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `billingContact` | boolean |  |
| `companyID` | number |  |
| `companyName` | string |  |
| `contactID` | number |  |
| `contactName` | string |  |
| `createdByUserID` | number |  |
| `createdByUserName` | string |  |
| `createdDateTime` | string |  |
| `emailInvoiceContact` | boolean |  |
| `emailNotificationsContact` | boolean |  |
| `lastModifiedByUserID` | object |  |
| `lastModifiedByUserName` | object |  |
| `lastModifiedDateTime` | object |  |
| `primaryContact` | boolean |  |
| `propertyID` | number |  |
| `propertyName` | string |  |
| `sMSNotificationsContact` | boolean |  |

## Native endpoint

Through the native Aspire API, this operation is `GET PropertyContacts` (base URL `https://{{credentials.environment}}.youraspire.com/`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-property-contacts.md) for the provider-specific parameters and requirements.

