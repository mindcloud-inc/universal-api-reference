# Jaicob: Retrieve Location



```
GET https://connect.mindcloud.co/v1/universal/jaicob/latest/actions/retrieve-location
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Jaicob `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/jaicob/latest/actions/retrieve-location?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/jaicob/latest/actions/retrieve-location?${params}`, {
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
| `id` | string | yes | Location identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "addressLine1": "string",
      "addressLine2": "string",
      "city": "string",
      "country": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "email": "ava@example.com",
      "id": "string",
      "isClient": true,
      "isHeadQuarter": true,
      "name": "Ava Chen",
      "phone": "string",
      "postcode": "string",
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
| `addressLine1` | string |  |
| `addressLine2` | string |  |
| `city` | string |  |
| `country` | string |  |
| `createdAt` | date |  |
| `email` | string |  |
| `id` | string |  |
| `isClient` | boolean |  |
| `isHeadQuarter` | boolean |  |
| `name` | string |  |
| `phone` | string |  |
| `postcode` | string |  |
| `state` | string |  |
| `updatedAt` | date |  |

## Native endpoint

Through the native Jaicob API, this operation is `GET /locations/public/[:id]` (base URL `https://api.jaicob.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-location.md) for the provider-specific parameters and requirements.

