# Pitchbox: List Contacts



```
GET https://connect.mindcloud.co/v1/universal/pitchbox/latest/actions/list-contacts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Pitchbox `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pitchbox/latest/actions/list-contacts?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pitchbox/latest/actions/list-contacts?${params}`, {
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
      "email": "ava@example.com",
      "enhancement": {
        "age": "string",
        "location": "string",
        "organizationName": "Ava Chen",
        "organizationTitle": "string"
      },
      "firstName": "Ava",
      "id": 1,
      "isUnsubscribed": true,
      "lastName": "Chen",
      "opportunityIds": [
        1
      ],
      "unsubscribedDate": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `email` | string |  |
| `enhancement.age` | string |  |
| `enhancement.location` | string |  |
| `enhancement.organizationName` | string |  |
| `enhancement.organizationTitle` | string |  |
| `firstName` | string |  |
| `id` | number |  |
| `isUnsubscribed` | boolean |  |
| `lastName` | string |  |
| `opportunityIds` | array<number> |  |
| `unsubscribedDate` | date |  |

## Native endpoint

Through the native Pitchbox API, this operation is `GET /api/contacts` (base URL `https://apiv2.pitchbox.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-contacts.md) for the provider-specific parameters and requirements.

