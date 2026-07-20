# Zoho FSM: List Contacts

Retrieves contacts from Zoho FSM.

```
GET https://connect.mindcloud.co/v1/universal/zohoFSM/latest/actions/list-contacts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoho FSM `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zohoFSM/latest/actions/list-contacts?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zohoFSM/latest/actions/list-contacts?${params}`, {
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
| `page` | number | no | Page number to fetch. |
| `perPage` | number | no | Number of records per page. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "$currency_symbol": "string",
      "$editable": true,
      "$inactive": true,
      "$permissions": {
        "delete": true,
        "edit": true,
        "read": true
      },
      "Created_By": {
        "email": "ava@example.com",
        "id": "string",
        "name": "Ava Chen"
      },
      "Created_Time": "2026-05-07T12:00:00.000Z",
      "Currency": "string",
      "Email": "ava@example.com",
      "Exchange_Rate": 1,
      "Full_Name": "Ava Chen",
      "id": "string",
      "Last_Name": "Chen",
      "Modified_By": {
        "email": "ava@example.com",
        "id": "string",
        "name": "Ava Chen"
      },
      "Modified_Time": "2026-05-07T12:00:00.000Z",
      "Owner": {
        "email": "ava@example.com",
        "id": "string",
        "name": "Ava Chen"
      },
      "Tax": {
        "Taxable": true
      },
      "ZBooks_Contact_Person": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `$currency_symbol` | string |  |
| `$editable` | boolean |  |
| `$inactive` | boolean |  |
| `$permissions.delete` | boolean |  |
| `$permissions.edit` | boolean |  |
| `$permissions.read` | boolean |  |
| `Created_By.email` | string |  |
| `Created_By.id` | string |  |
| `Created_By.name` | string |  |
| `Created_Time` | date |  |
| `Currency` | string |  |
| `Email` | string |  |
| `Exchange_Rate` | number |  |
| `Full_Name` | string |  |
| `id` | string |  |
| `Last_Name` | string |  |
| `Modified_By.email` | string |  |
| `Modified_By.id` | string |  |
| `Modified_By.name` | string |  |
| `Modified_Time` | date |  |
| `Owner.email` | string |  |
| `Owner.id` | string |  |
| `Owner.name` | string |  |
| `Tax.Taxable` | boolean |  |
| `ZBooks_Contact_Person` | boolean |  |

## Native endpoint

Through the native Zoho FSM API, this operation is `GET /Contacts` (base URL `{{credentials.accessTokenRequest.api_domain}}/fsm/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-contacts.md) for the provider-specific parameters and requirements.

