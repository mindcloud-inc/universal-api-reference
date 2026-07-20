# Pitchbox: Get Contact By Id



```
GET https://connect.mindcloud.co/v1/universal/pitchbox/latest/actions/get-contact-by-id
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Pitchbox `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pitchbox/latest/actions/get-contact-by-id?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pitchbox/latest/actions/get-contact-by-id?${params}`, {
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
| `id` | string | yes | Pitchbox contact identifier |

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
      "lastCommunicationDate": "2026-05-07T12:00:00.000Z",
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
| `lastCommunicationDate` | date |  |
| `lastName` | string |  |
| `opportunityIds` | array<number> |  |
| `unsubscribedDate` | date |  |

## Native endpoint

Through the native Pitchbox API, this operation is `GET /api/contacts/:id` (base URL `https://apiv2.pitchbox.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-contact-by-id.md) for the provider-specific parameters and requirements.

