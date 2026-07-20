# RAYNET CRM: List Contacts



```
GET https://connect.mindcloud.co/v1/universal/rAYNETCRM/latest/actions/list-contacts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a RAYNET CRM `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [filtering](../filtering.md) (`where`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/rAYNETCRM/latest/actions/list-contacts?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/rAYNETCRM/latest/actions/list-contacts?${params}`, {
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
      "activeUserAccount": true,
      "companyAddress": {
        "address": {
          "country": "string",
          "countryCode": "string"
        }
      },
      "contactInfo": {
        "email": "ava@example.com",
        "email2": "ava@example.com",
        "tel1": "string"
      },
      "firstName": "Ava",
      "id": 1,
      "keyman": true,
      "lastName": "Chen",
      "owner": {
        "fullName": "Ava Chen"
      },
      "primaryRelationship": {
        "company": {
          "id": 1,
          "name": "Ava Chen"
        },
        "type": "string"
      },
      "rowInfo": {
        "createdAt": "2026-05-07T12:00:00.000Z"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `activeUserAccount` | boolean |  |
| `companyAddress.address.country` | string |  |
| `companyAddress.address.countryCode` | string |  |
| `contactInfo.email` | string |  |
| `contactInfo.email2` | string |  |
| `contactInfo.tel1` | string |  |
| `firstName` | string |  |
| `id` | number |  |
| `keyman` | boolean |  |
| `lastName` | string |  |
| `owner.fullName` | string |  |
| `primaryRelationship.company.id` | number |  |
| `primaryRelationship.company.name` | string |  |
| `primaryRelationship.type` | string |  |
| `rowInfo.createdAt` | date |  |

## Native endpoint

Through the native RAYNET CRM API, this operation is `GET person/` (base URL `https://app.raynetcrm.com/api/v2/`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-contacts.md) for the provider-specific parameters and requirements.

