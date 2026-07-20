# Joonto: List SMS Contacts



```
GET https://connect.mindcloud.co/v1/universal/joonto/latest/actions/list-sms-contacts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Joonto `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/joonto/latest/actions/list-sms-contacts?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/joonto/latest/actions/list-sms-contacts?${params}`, {
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
| `skip` | number | no |  |
| `take` | number | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "active": true,
      "billingCycle": "string",
      "companyName": "Ava Chen",
      "count": 1,
      "dateCreated": "2026-05-07T12:00:00.000Z",
      "email": "ava@example.com",
      "id": 1,
      "imageId": 1,
      "joontoPhone": "string",
      "joontoPhonePretty": "string",
      "locked": true,
      "name": "Ava Chen",
      "phone": "string",
      "phonePretty": "string",
      "phoneVerified": true,
      "plan": "string",
      "timeZone": "string",
      "timeZoneFriendly": "string",
      "timeZoneHours": 1,
      "timeZoneHoursAdd": 1,
      "userManagerStatus": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `active` | boolean |  |
| `billingCycle` | string |  |
| `companyName` | string |  |
| `count` | number |  |
| `dateCreated` | date |  |
| `email` | string |  |
| `id` | number |  |
| `imageId` | number |  |
| `joontoPhone` | string |  |
| `joontoPhonePretty` | string |  |
| `locked` | boolean |  |
| `name` | string |  |
| `phone` | string |  |
| `phonePretty` | string |  |
| `phoneVerified` | boolean |  |
| `plan` | string |  |
| `timeZone` | string |  |
| `timeZoneFriendly` | string |  |
| `timeZoneHours` | number |  |
| `timeZoneHoursAdd` | number |  |
| `userManagerStatus` | string |  |

## Native endpoint

Through the native Joonto API, this operation is `POST /api/Users/GetSmsContacts` (base URL `https://api.joonto.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-sms-contacts.md) for the provider-specific parameters and requirements.

