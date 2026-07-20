# Refiner: Get Contact

Retrieves a contact from Refiner by ID or email.

```
GET https://connect.mindcloud.co/v1/universal/refiner/latest/actions/get-contact
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Refiner `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/refiner/latest/actions/get-contact?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/refiner/latest/actions/get-contact?${params}`, {
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
| `id` | string | no | Look up the contact by your own user ID. |
| `email` | string | no | Look up the contact by email address. |
| `uuid` | string | no | Look up the contact by the Refiner UUID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "account": {},
      "attributes": {},
      "displayName": "Ava Chen",
      "email": "ava@example.com",
      "firstSeenAt": "2026-05-07T12:00:00.000Z",
      "lastSeenAt": "2026-05-07T12:00:00.000Z",
      "remoteId": "string",
      "segments": [
        {}
      ],
      "uuid": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `account` | object |  |
| `attributes` | object |  |
| `displayName` | string |  |
| `email` | string |  |
| `firstSeenAt` | date |  |
| `lastSeenAt` | date |  |
| `remoteId` | string |  |
| `segments` | array<object> |  |
| `uuid` | string |  |

## Native endpoint

Through the native Refiner API, this operation is `GET /contact` (base URL `https://api.refiner.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-contact.md) for the provider-specific parameters and requirements.

