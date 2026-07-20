# Loyverse: Get Store

Retrieves a store record from Loyverse.

```
GET https://connect.mindcloud.co/v1/universal/loyverse/latest/actions/get-store
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Loyverse `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/loyverse/latest/actions/get-store?connectionId=$CONNECTION_ID&storeId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "storeId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/loyverse/latest/actions/get-store?${params}`, {
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
| `storeId` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "address": "string",
      "city": "string",
      "country": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "deletedAt": "2026-05-07T12:00:00.000Z",
      "description": "string",
      "id": "string",
      "name": "Ava Chen",
      "phoneNumber": "string",
      "postalCode": "string",
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
| `address` | string |  |
| `city` | string |  |
| `country` | string | Country format (ISO alpha-2) |
| `createdAt` | date | The time when this resource was created (ISO 8601 format, e.g. 2020-03-25T19:55:23.077Z) |
| `deletedAt` | date | The time when this resource was deleted (ISO 8601 format, e.g. 2020-04-02T23:45:20.050Z) |
| `description` | string |  |
| `id` | string |  |
| `name` | string |  |
| `phoneNumber` | string |  |
| `postalCode` | string |  |
| `state` | string |  |
| `updatedAt` | date | The time when this resource was updated (ISO 8601 format, e.g. 2020-03-30T08:05:10.020Z) |

## Native endpoint

Through the native Loyverse API, this operation is `GET /stores/:store_id` (base URL `https://api.loyverse.com/v1.0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-store.md) for the provider-specific parameters and requirements.

