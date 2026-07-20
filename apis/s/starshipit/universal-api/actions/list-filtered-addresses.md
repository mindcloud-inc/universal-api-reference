# Starshipit: List Filtered Addresses



```
GET https://connect.mindcloud.co/v1/universal/starshipit/latest/actions/list-filtered-addresses
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Starshipit `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/starshipit/latest/actions/list-filtered-addresses?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/starshipit/latest/actions/list-filtered-addresses?${params}`, {
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
| `page` | number | no | Which page of the address book to return |
| `pageSize` | number | no | Number of records per page |
| `sort` | string | no | Sort by column. Available values: None, Name, Company, Street, Suburb, PostCode, City, State, Country, Code, Phone, Email |
| `sortDirection` | string | no | Sort direction for the sort column. Available values: None, Ascending, Descending |

## Response

```json
{
  "success": true,
  "data": [
    {
      "addresses": [
        {
          "building": "string",
          "city": "string",
          "code": "string",
          "company": "string",
          "country": "string",
          "email": "ava@example.com",
          "id": 1,
          "name": "Ava Chen",
          "postCode": "string",
          "state": "string",
          "street": "string",
          "suburb": "string",
          "telephone": "string"
        }
      ],
      "success": true,
      "totalCount": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `addresses` | array<object> |  |
| `addresses[].building` | string |  |
| `addresses[].city` | string |  |
| `addresses[].code` | string |  |
| `addresses[].company` | string |  |
| `addresses[].country` | string |  |
| `addresses[].email` | string |  |
| `addresses[].id` | number |  |
| `addresses[].name` | string |  |
| `addresses[].postCode` | string |  |
| `addresses[].state` | string |  |
| `addresses[].street` | string |  |
| `addresses[].suburb` | string |  |
| `addresses[].telephone` | string |  |
| `success` | boolean |  |
| `totalCount` | number |  |

## Native endpoint

Through the native Starshipit API, this operation is `GET /addressbook/filtered` (base URL `https://api.starshipit.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-filtered-addresses.md) for the provider-specific parameters and requirements.

