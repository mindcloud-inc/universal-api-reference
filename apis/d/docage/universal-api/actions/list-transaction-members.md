# Docage: List Transaction Members

Retrieves the members of a Docage transaction.

```
GET https://connect.mindcloud.co/v1/universal/docage/latest/actions/list-transaction-members
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Docage `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/docage/latest/actions/list-transaction-members?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/docage/latest/actions/list-transaction-members?${params}`, {
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
| `id` | string | yes | The Docage transaction ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "Company": "string",
      "ContactId": "string",
      "DocageUserId": "string",
      "Email": "ava@example.com",
      "FirstName": "Ava",
      "FriendlyName": "Ava Chen",
      "IsFollower": true,
      "IsFormFiller": true,
      "IsSignatory": true,
      "IsValidator": true,
      "LastName": "Chen",
      "MemberRole": 1,
      "Mobile": "string",
      "Phone": "string",
      "SignMode": 1,
      "TransactionId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `Company` | string |  |
| `ContactId` | string |  |
| `DocageUserId` | string |  |
| `Email` | string |  |
| `FirstName` | string |  |
| `FriendlyName` | string |  |
| `IsFollower` | boolean |  |
| `IsFormFiller` | boolean |  |
| `IsSignatory` | boolean |  |
| `IsValidator` | boolean |  |
| `LastName` | string |  |
| `MemberRole` | number |  |
| `Mobile` | string |  |
| `Phone` | string |  |
| `SignMode` | number |  |
| `TransactionId` | string |  |

## Native endpoint

Through the native Docage API, this operation is `GET /Transactions/GetTransactionMembers/:id` (base URL `https://api.docage.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-transaction-members.md) for the provider-specific parameters and requirements.

