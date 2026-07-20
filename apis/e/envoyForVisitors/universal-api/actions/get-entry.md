# Envoy for Visitors: Get Entry

Retrieves an entry from Envoy for Visitors.

```
GET https://connect.mindcloud.co/v1/universal/envoyForVisitors/latest/actions/get-entry
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Envoy for Visitors `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/envoyForVisitors/latest/actions/get-entry?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/envoyForVisitors/latest/actions/get-entry?${params}`, {
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
| `id` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "agreementsStatus": "string",
      "customFields": [
        {}
      ],
      "email": "ava@example.com",
      "flowId": "string",
      "fullName": "Ava Chen",
      "id": "string",
      "isDelivery": true,
      "locationId": "string",
      "signedInAt": "2026-05-07T12:00:00.000Z",
      "signedInVia": "string",
      "signedOutAt": "2026-05-07T12:00:00.000Z",
      "signedOutVia": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `agreementsStatus` | string |  |
| `customFields` | array<object> |  |
| `email` | string |  |
| `flowId` | string |  |
| `fullName` | string |  |
| `id` | string |  |
| `isDelivery` | boolean |  |
| `locationId` | string |  |
| `signedInAt` | date |  |
| `signedInVia` | string |  |
| `signedOutAt` | date |  |
| `signedOutVia` | string |  |

## Native endpoint

Through the native Envoy for Visitors API, this operation is `GET /entries/:id` (base URL `https://api.envoy.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-entry.md) for the provider-specific parameters and requirements.

