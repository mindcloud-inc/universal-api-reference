# Eventee: List Participants

Retrieves participants from Eventee.

```
GET https://connect.mindcloud.co/v1/universal/eventee/latest/actions/list-participants
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Eventee `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/eventee/latest/actions/list-participants?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/eventee/latest/actions/list-participants?${params}`, {
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
      "checkedAt": "2026-05-07T12:00:00.000Z",
      "company": "string",
      "email": "ava@example.com",
      "firstName": "Ava",
      "groupId": 1,
      "id": 1,
      "lastName": "Chen",
      "name": "Ava Chen",
      "position": "string",
      "registeredAt": "2026-05-07T12:00:00.000Z",
      "role": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `checkedAt` | date | Check-in datetime. |
| `company` | string | Participant company. |
| `email` | string | Participant email. |
| `firstName` | string | Participant first name. |
| `groupId` | number | Assigned group ID. |
| `id` | number | Participant ID. |
| `lastName` | string | Participant last name. |
| `name` | string | Participant full name. |
| `position` | string | Participant position title. |
| `registeredAt` | date | Registration datetime. |
| `role` | string | Participant role code. |

## Native endpoint

Through the native Eventee API, this operation is `GET /participants` (base URL `https://api.eventee.com/public/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-participants.md) for the provider-specific parameters and requirements.

