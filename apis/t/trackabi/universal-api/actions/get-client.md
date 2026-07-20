# Trackabi: Get Client

Retrieves a client from Trackabi.

```
GET https://connect.mindcloud.co/v1/universal/trackabi/latest/actions/get-client
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Trackabi `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/trackabi/latest/actions/get-client?connectionId=$CONNECTION_ID&clientId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "clientId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/trackabi/latest/actions/get-client?${params}`, {
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
| `clientId` | number | yes | The unique ID of the client. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "address": "string",
      "contactPerson": "string",
      "costHourlyRate": 1,
      "currency": "string",
      "email": "ava@example.com",
      "hourlyRate": 1,
      "id": 1,
      "logo": "string",
      "name": "Ava Chen",
      "notes": "string",
      "phone": "string",
      "shortName": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `address` | string |  |
| `contactPerson` | string |  |
| `costHourlyRate` | number |  |
| `currency` | string |  |
| `email` | string |  |
| `hourlyRate` | number |  |
| `id` | number |  |
| `logo` | string |  |
| `name` | string |  |
| `notes` | string |  |
| `phone` | string |  |
| `shortName` | string |  |

## Native endpoint

Through the native Trackabi API, this operation is `GET /api/v1/clients/:clientId` (base URL `https://api.trackabi.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-client.md) for the provider-specific parameters and requirements.

