# Bexio: Search Contacts

Finds contacts in Bexio by search criteria.

```
GET https://connect.mindcloud.co/v1/universal/bexio/latest/actions/search-contacts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Bexio `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bexio/latest/actions/search-contacts?connectionId=$CONNECTION_ID&input%5B%5D.field=address&input%5B%5D.value=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "input[].field": "address",
  "input[].value": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/bexio/latest/actions/search-contacts?${params}`, {
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
| `input[]` | array<object> | no | Array of contact search clauses sent as the request body. |
| `input[].field` | list<string> | yes | Contact field to search over. One of: `address`, `city`, `contact_group_ids`, `contact_type_id`, `country_id`, `fax`, `id`, `mail`, `mail_second`, `name_1`, `name_2`, `nr`, `phone_fixed`, `phone_mobile`, `postcode`, `updated_at`, `user_id`. |
| `input[].criteria` | list<string> | no | Comparison operator for the search clause. Defaults to like. One of: `!=`, `<`, `<=`, `=`, `>`, `>=`, `equal`, `greater_equal`, `greater_than`, `in`, `is_null`, `less_equal`, `less_than`, `like`, `not_equal`, `not_in`, `not_like`, `not_null`. Default: `like`. |
| `input[].value` | string | yes | Value to search for. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "address": "string",
      "addressAddition": {},
      "birthday": "2026-05-07T12:00:00.000Z",
      "city": "string",
      "contactBranchIds": {},
      "contactGroupIds": "string",
      "contactTypeId": 1,
      "countryId": 1,
      "fax": "string",
      "houseNumber": "string",
      "id": 1,
      "isLead": true,
      "languageId": {},
      "mail": {},
      "mailSecond": {},
      "name1": "Ava Chen",
      "name2": "Ava Chen",
      "nr": "string",
      "ownerId": 1,
      "phoneFixed": {},
      "phoneFixedSecond": {},
      "phoneMobile": "string",
      "postcode": "string",
      "remarks": "string",
      "salutationForm": {},
      "salutationId": 1,
      "skypeName": "Ava Chen",
      "streetName": "Ava Chen",
      "titleId": {},
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "url": "https://example.com",
      "userId": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `address` | string |  |
| `addressAddition` | object |  |
| `birthday` | date |  |
| `city` | string |  |
| `contactBranchIds` | object |  |
| `contactGroupIds` | string |  |
| `contactTypeId` | number |  |
| `countryId` | number |  |
| `fax` | string |  |
| `houseNumber` | string |  |
| `id` | number |  |
| `isLead` | boolean |  |
| `languageId` | object |  |
| `mail` | object |  |
| `mailSecond` | object |  |
| `name1` | string |  |
| `name2` | string |  |
| `nr` | string |  |
| `ownerId` | number |  |
| `phoneFixed` | object |  |
| `phoneFixedSecond` | object |  |
| `phoneMobile` | string |  |
| `postcode` | string |  |
| `remarks` | string |  |
| `salutationForm` | object |  |
| `salutationId` | number |  |
| `skypeName` | string |  |
| `streetName` | string |  |
| `titleId` | object |  |
| `updatedAt` | date |  |
| `url` | string |  |
| `userId` | number |  |

## Native endpoint

Through the native Bexio API, this operation is `POST /2.0/contact/search` (base URL `https://api.bexio.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-contacts.md) for the provider-specific parameters and requirements.

