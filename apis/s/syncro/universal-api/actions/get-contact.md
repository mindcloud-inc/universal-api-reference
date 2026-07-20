# Syncro: Get Contact

Retrieves a contact from Syncro by ID.

```
GET https://connect.mindcloud.co/v1/universal/syncro/latest/actions/get-contact
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Syncro `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/syncro/latest/actions/get-contact?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/syncro/latest/actions/get-contact?${params}`, {
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
| `id` | number | yes | The Syncro contact ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "accountId": 1,
      "address1": "string",
      "city": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "customerId": 1,
      "email": "ava@example.com",
      "id": 1,
      "name": "Ava Chen",
      "optOut": true,
      "phone": "string",
      "processedPhone": "string",
      "sinceUpdatedAt": "2026-05-07T12:00:00.000Z",
      "state": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accountId` | number |  |
| `address1` | string |  |
| `city` | string |  |
| `createdAt` | date |  |
| `customerId` | number |  |
| `email` | string |  |
| `id` | number |  |
| `name` | string |  |
| `optOut` | boolean |  |
| `phone` | string |  |
| `processedPhone` | string |  |
| `sinceUpdatedAt` | date |  |
| `state` | string |  |
| `updatedAt` | date |  |

## Native endpoint

Through the native Syncro API, this operation is `GET /contacts/:id` (base URL `https://mindcloud.syncromsp.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-contact.md) for the provider-specific parameters and requirements.

