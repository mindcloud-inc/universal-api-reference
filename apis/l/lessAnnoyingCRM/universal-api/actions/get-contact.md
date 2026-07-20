# Less Annoying CRM: Get Contact



```
GET https://connect.mindcloud.co/v1/universal/lessAnnoyingCRM/latest/actions/get-contact
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Less Annoying CRM `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/lessAnnoyingCRM/latest/actions/get-contact?connectionId=$CONNECTION_ID&contactId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "contactId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/lessAnnoyingCRM/latest/actions/get-contact?${params}`, {
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
| `contactId` | string | yes | The contact or company Id to fetch. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "assignedTo": 1,
      "backgroundInfo": "string",
      "companyId": "string",
      "companyMetaData": {
        "companyName": "Ava Chen"
      },
      "companyName": "Ava Chen",
      "contactId": "string",
      "dateCreated": "2026-05-07T12:00:00.000Z",
      "isCompany": true,
      "jobTitle": "string",
      "lastUpdate": "2026-05-07T12:00:00.000Z",
      "name": {
        "firstName": "Ava",
        "lastName": "Chen",
        "middleName": "Ava Chen",
        "salutation": "Ava Chen",
        "suffix": "Ava Chen"
      },
      "userMetaData": {
        "firstName": "Ava",
        "lastName": "Chen"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `assignedTo` | number |  |
| `backgroundInfo` | string |  |
| `companyId` | string |  |
| `companyMetaData.companyName` | string |  |
| `companyName` | string |  |
| `contactId` | string |  |
| `dateCreated` | date |  |
| `isCompany` | boolean |  |
| `jobTitle` | string |  |
| `lastUpdate` | date |  |
| `name.firstName` | string |  |
| `name.lastName` | string |  |
| `name.middleName` | string |  |
| `name.salutation` | string |  |
| `name.suffix` | string |  |
| `userMetaData.firstName` | string |  |
| `userMetaData.lastName` | string |  |

## Native endpoint

Through the native Less Annoying CRM API, this operation is `POST /` (base URL `https://api.lessannoyingcrm.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-contact.md) for the provider-specific parameters and requirements.

