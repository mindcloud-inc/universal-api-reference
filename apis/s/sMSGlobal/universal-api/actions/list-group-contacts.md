# SMSGlobal: List Group Contacts

Retrieves contacts from an SMSGlobal contact group.

```
GET https://connect.mindcloud.co/v1/universal/sMSGlobal/latest/actions/list-group-contacts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SMSGlobal `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sMSGlobal/latest/actions/list-group-contacts?connectionId=$CONNECTION_ID&groupId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "groupId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sMSGlobal/latest/actions/list-group-contacts?${params}`, {
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
| `groupId` | number | yes | The contact group identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "contacts": [
        {
          "displayName": "Ava Chen",
          "emailAddress": "ava@example.com",
          "familyName": "Ava Chen",
          "givenName": "Ava Chen",
          "id": 1,
          "msisdn": "string"
        }
      ],
      "limit": 1,
      "offset": 1,
      "total": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `contacts[].displayName` | string | Contact display name. |
| `contacts[].emailAddress` | string | Contact email address. |
| `contacts[].familyName` | string | Contact surname. |
| `contacts[].givenName` | string | Contact given name. |
| `contacts[].id` | number | Contact identifier. |
| `contacts[].msisdn` | string | Contact mobile number. |
| `limit` | number | Number of contacts returned. |
| `offset` | number | Pagination offset. |
| `total` | number | Total number of contacts in the group. |

## Native endpoint

Through the native SMSGlobal API, this operation is `GET /v2/group/:groupId/contacts` (base URL `https://api.smsglobal.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-group-contacts.md) for the provider-specific parameters and requirements.

