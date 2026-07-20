# Growby: List Contacts

Retrieves contacts from Growby.

```
GET https://connect.mindcloud.co/v1/universal/growby/latest/actions/list-contacts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Growby `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/growby/latest/actions/list-contacts?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/growby/latest/actions/list-contacts?${params}`, {
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
| `pageNumber` | number | no | Page number to fetch. Growby documents values from 1 to 20. Default: `1`. |
| `pageSize` | number | no | Number of contacts to return per page. Growby documents values from 1 to 20. Default: `1`. |
| `sortColumn` | string | no | Column name used for sorting. Supported values are Id, AccountId, FirstName, LastName, Email, MobileNumber, City, and State. Default: `Id`. |
| `sortOrder` | string | no | Sort direction. Supported values are ASC or DESC. Default: `ASC`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "accountId": 1,
      "address": "string",
      "anniversaryDate": {},
      "birthdate": {},
      "city": "string",
      "column1": "string",
      "column10": "string",
      "column11": "string",
      "column12": "string",
      "column13": "string",
      "column14": "string",
      "column15": "string",
      "column2": "string",
      "column3": "string",
      "column4": "string",
      "column5": "string",
      "column6": "string",
      "column7": "string",
      "column8": "string",
      "column9": "string",
      "companyName": "Ava Chen",
      "country": "string",
      "countryCode": 1,
      "customerIdPartition": 1,
      "emailId": "ava@example.com",
      "firstName": "Ava",
      "id": 1,
      "isSubscribed": 1,
      "lastName": "Chen",
      "middleName": "Ava Chen",
      "mobileNumber": "string",
      "nationalNumber": "string",
      "nickName": "Ava Chen",
      "source": "string",
      "state": "string",
      "website": "string",
      "weddingDate": {},
      "zipCode": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accountId` | number |  |
| `address` | string |  |
| `anniversaryDate` | object |  |
| `birthdate` | object |  |
| `city` | string |  |
| `column1` | string |  |
| `column10` | string |  |
| `column11` | string |  |
| `column12` | string |  |
| `column13` | string |  |
| `column14` | string |  |
| `column15` | string |  |
| `column2` | string |  |
| `column3` | string |  |
| `column4` | string |  |
| `column5` | string |  |
| `column6` | string |  |
| `column7` | string |  |
| `column8` | string |  |
| `column9` | string |  |
| `companyName` | string |  |
| `country` | string |  |
| `countryCode` | number |  |
| `customerIdPartition` | number |  |
| `emailId` | string |  |
| `firstName` | string |  |
| `id` | number |  |
| `isSubscribed` | number |  |
| `lastName` | string |  |
| `middleName` | string |  |
| `mobileNumber` | string |  |
| `nationalNumber` | string |  |
| `nickName` | string |  |
| `source` | string |  |
| `state` | string |  |
| `website` | string |  |
| `weddingDate` | object |  |
| `zipCode` | string |  |

## Native endpoint

Through the native Growby API, this operation is `GET /devapi/contacts` (base URL `https://api.growby.net`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-contacts.md) for the provider-specific parameters and requirements.

