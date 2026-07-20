# Fireberry: List Contacts

Retrieves all contact records from Fireberry.

```
GET https://connect.mindcloud.co/v1/universal/fireberry/latest/actions/list-contacts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Fireberry `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/fireberry/latest/actions/list-contacts?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/fireberry/latest/actions/list-contacts?${params}`, {
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
      "accountid": "string",
      "accountname": "Ava Chen",
      "contactid": "string",
      "createdby": "string",
      "createdbyname": "Ava Chen",
      "createdon": "2026-05-07T12:00:00.000Z",
      "department": "string",
      "description": "string",
      "emailaddress1": "ava@example.com",
      "firstname": "Ava",
      "fullname": "Ava Chen",
      "isvalidforemail": "ava@example.com",
      "isvalidforemailcode": 1,
      "jobtitle": "string",
      "lastname": "Chen",
      "mobilephone1": "string",
      "modifiedby": "string",
      "modifiedbyname": "Ava Chen",
      "modifiedon": "2026-05-07T12:00:00.000Z",
      "ownerid": "string",
      "ownername": "Ava Chen",
      "salutation": "string",
      "salutationname": "Ava Chen",
      "telephone1": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accountid` | string |  |
| `accountname` | string |  |
| `contactid` | string |  |
| `createdby` | string |  |
| `createdbyname` | string |  |
| `createdon` | date |  |
| `department` | string |  |
| `description` | string |  |
| `emailaddress1` | string |  |
| `firstname` | string |  |
| `fullname` | string |  |
| `isvalidforemail` | string |  |
| `isvalidforemailcode` | number |  |
| `jobtitle` | string |  |
| `lastname` | string |  |
| `mobilephone1` | string |  |
| `modifiedby` | string |  |
| `modifiedbyname` | string |  |
| `modifiedon` | date |  |
| `ownerid` | string |  |
| `ownername` | string |  |
| `salutation` | string |  |
| `salutationname` | string |  |
| `telephone1` | string |  |

## Native endpoint

Through the native Fireberry API, this operation is `GET /api/record/contact` (base URL `https://api.fireberry.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-contacts.md) for the provider-specific parameters and requirements.

