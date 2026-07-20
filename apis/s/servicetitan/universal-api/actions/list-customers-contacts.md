# ServiceTitan: List Customers Contacts

Retrieves customer contacts from ServiceTitan.

```
GET https://connect.mindcloud.co/v1/universal/servicetitan/latest/actions/list-customers-contacts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ServiceTitan `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/servicetitan/latest/actions/list-customers-contacts?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/servicetitan/latest/actions/list-customers-contacts?${params}`, {
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
| `modifiedOnOrAfter` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdOn": "string",
      "id": 1,
      "memo": {},
      "modifiedOn": "string",
      "phoneSettings": {},
      "preferences": {
        "invoiceStatementNotification": true,
        "jobRemindersEnabled": true,
        "marketingUpdatesEnabled": true
      },
      "type": "string",
      "value": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdOn` | string |  |
| `id` | number |  |
| `memo` | object |  |
| `modifiedOn` | string |  |
| `phoneSettings` | object |  |
| `preferences.invoiceStatementNotification` | boolean |  |
| `preferences.jobRemindersEnabled` | boolean |  |
| `preferences.marketingUpdatesEnabled` | boolean |  |
| `type` | string |  |
| `value` | string |  |

## Native endpoint

Through the native ServiceTitan API, this operation is `GET crm/v2/tenant/{{credentials.tenant}}/customers/contacts` (base URL `https://{{credentials.baseUrl}}/`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-customers-contacts.md) for the provider-specific parameters and requirements.

