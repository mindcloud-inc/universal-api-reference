# Docage: List Transactions

Retrieves accessible transactions from Docage.

```
GET https://connect.mindcloud.co/v1/universal/docage/latest/actions/list-transactions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Docage `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/docage/latest/actions/list-transactions?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/docage/latest/actions/list-transactions?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "CompletionEmailSubject": "ava@example.com",
      "DaysBeforeEnding": 1,
      "EndDate": "string",
      "FormEmailSubject": "ava@example.com",
      "InvitationEmailBody": "ava@example.com",
      "InvitationEmailSubject": "ava@example.com",
      "IsTest": true,
      "MaximumReminders": 1,
      "Name": "Ava Chen",
      "RefusalEmailSubject": "ava@example.com",
      "Reminder": 1,
      "ReminderEmailBody": "ava@example.com",
      "ReminderEmailSubject": "ava@example.com",
      "SalePrice": 1,
      "SignatureEmailSubject": "ava@example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `CompletionEmailSubject` | string |  |
| `DaysBeforeEnding` | number |  |
| `EndDate` | string |  |
| `FormEmailSubject` | string |  |
| `InvitationEmailBody` | string |  |
| `InvitationEmailSubject` | string |  |
| `IsTest` | boolean |  |
| `MaximumReminders` | number |  |
| `Name` | string |  |
| `RefusalEmailSubject` | string |  |
| `Reminder` | number |  |
| `ReminderEmailBody` | string |  |
| `ReminderEmailSubject` | string |  |
| `SalePrice` | number |  |
| `SignatureEmailSubject` | string |  |

## Native endpoint

Through the native Docage API, this operation is `GET /Transactions` (base URL `https://api.docage.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-transactions.md) for the provider-specific parameters and requirements.

