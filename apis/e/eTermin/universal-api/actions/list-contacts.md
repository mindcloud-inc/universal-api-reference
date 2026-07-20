# eTermin: List Contacts

Retrieves contacts from eTermin.

```
GET https://connect.mindcloud.co/v1/universal/eTermin/latest/actions/list-contacts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a eTermin `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/eTermin/latest/actions/list-contacts?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/eTermin/latest/actions/list-contacts?${params}`, {
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
| `email` | string | no | E-Mail of the contact |
| `id` | string | no | ExternalID of the contact |
| `cid` | string | no | CID of the contact |
| `creationdate` | string | no | Displays all contacts that were created on this date |
| `creationdateall` | string | no | Displays all contacts that were created since this date |

## Response

```json
{
  "success": true,
  "data": [
    {
      "activated": true,
      "additional1": "string",
      "additional10": "string",
      "additional11": "string",
      "additional12": "string",
      "additional13": "string",
      "additional14": "string",
      "additional15": "string",
      "additional16": "string",
      "additional17": "string",
      "additional18": "string",
      "additional19": "string",
      "additional2": "string",
      "additional20": "string",
      "additional3": "string",
      "additional4": "string",
      "additional5": "string",
      "additional6": "string",
      "additional7": "string",
      "additional8": "string",
      "additional9": "string",
      "birthday": "string",
      "cid": 1,
      "city": "string",
      "company": "string",
      "country": "string",
      "creationDate": "string",
      "customerNumber": "string",
      "email": "ava@example.com",
      "externalId": "string",
      "firstName": "Ava",
      "language": "string",
      "lastAppointmentDate": "string",
      "lastName": "Chen",
      "limitedServices": true,
      "loginId": "string",
      "newsletter": true,
      "notes": "string",
      "phone": "string",
      "salutation": "string",
      "state": "string",
      "street": "string",
      "tags": "string",
      "title": "string",
      "zip": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `activated` | boolean |  |
| `additional1` | string |  |
| `additional10` | string |  |
| `additional11` | string |  |
| `additional12` | string |  |
| `additional13` | string |  |
| `additional14` | string |  |
| `additional15` | string |  |
| `additional16` | string |  |
| `additional17` | string |  |
| `additional18` | string |  |
| `additional19` | string |  |
| `additional2` | string |  |
| `additional20` | string |  |
| `additional3` | string |  |
| `additional4` | string |  |
| `additional5` | string |  |
| `additional6` | string |  |
| `additional7` | string |  |
| `additional8` | string |  |
| `additional9` | string |  |
| `birthday` | string |  |
| `cid` | number |  |
| `city` | string |  |
| `company` | string |  |
| `country` | string |  |
| `creationDate` | string |  |
| `customerNumber` | string |  |
| `email` | string |  |
| `externalId` | string |  |
| `firstName` | string |  |
| `language` | string |  |
| `lastAppointmentDate` | string |  |
| `lastName` | string |  |
| `limitedServices` | boolean |  |
| `loginId` | string |  |
| `newsletter` | boolean |  |
| `notes` | string |  |
| `phone` | string |  |
| `salutation` | string |  |
| `state` | string |  |
| `street` | string |  |
| `tags` | string |  |
| `title` | string |  |
| `zip` | string |  |

## Native endpoint

Through the native eTermin API, this operation is `GET /api/contact` (base URL `https://www.etermin.net`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-contacts.md) for the provider-specific parameters and requirements.

