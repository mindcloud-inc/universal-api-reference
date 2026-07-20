# Atera: Get contact

Retrieves a contact from Atera by ID.

```
GET https://connect.mindcloud.co/v1/universal/atera/latest/actions/get-contact
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Atera `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/atera/latest/actions/get-contact?connectionId=$CONNECTION_ID&contactId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "contactId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/atera/latest/actions/get-contact?${params}`, {
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
| `contactId` | number | yes | System contact ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "Archived": true,
      "CreatedOn": "string",
      "CustomerID": 1,
      "CustomerName": "Ava Chen",
      "Email": "ava@example.com",
      "EndUserID": 1,
      "Firstname": "Ava",
      "InIgnoreMode": true,
      "IsContactPerson": true,
      "JobTitle": "string",
      "LastModified": "string",
      "Lastname": "Chen",
      "Phone": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `Archived` | boolean |  |
| `CreatedOn` | string |  |
| `CustomerID` | number |  |
| `CustomerName` | string |  |
| `Email` | string |  |
| `EndUserID` | number |  |
| `Firstname` | string |  |
| `InIgnoreMode` | boolean |  |
| `IsContactPerson` | boolean |  |
| `JobTitle` | string |  |
| `LastModified` | string |  |
| `Lastname` | string |  |
| `Phone` | string |  |

## Native endpoint

Through the native Atera API, this operation is `GET /api/v3/contacts/:contactId` (base URL `https://app.atera.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-contact.md) for the provider-specific parameters and requirements.

