# Loyverse: List Stores

Retrieves store records from the Loyverse account.

```
GET https://connect.mindcloud.co/v1/universal/loyverse/latest/actions/list-stores
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Loyverse `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/loyverse/latest/actions/list-stores?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/loyverse/latest/actions/list-stores?${params}`, {
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
| `storeIds` | string | no | Return only store specified by a comma-separated list of IDs |
| `createdAtMin` | date | no | Show resources created after date (ISO 8601 format, e.g: 2020-03-30T18:30:00.000Z) |
| `createdAtMax` | date | no | Show resources created before date (ISO 8601 format, e.g: 2020-03-30T18:30:00.000Z) |
| `updatedAtMin` | string | no | Show resources updated after date (ISO 8601 format, e.g: 2020-03-30T18:30:00.000Z) |
| `updatedAtMax` | string | no | Show resources updated before date (ISO 8601 format, e.g: 2020-03-30T18:30:00.000Z) |
| `showDeleted` | boolean | no | Show deleted modifiers and modifier options |

## Response

```json
{
  "success": true,
  "data": [
    {
      "stores": [
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
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `stores` | array<object> |  |
| `stores[].address` | string |  |
| `stores[].city` | string |  |
| `stores[].country` | string | Country format (ISO alpha-2) |
| `stores[].createdAt` | date | The time when this resource was created (ISO 8601 format, e.g. 2020-03-25T19:55:23.077Z) |
| `stores[].deletedAt` | date | The time when this resource was deleted (ISO 8601 format, e.g. 2020-04-02T23:45:20.050Z) |
| `stores[].description` | string |  |
| `stores[].id` | string |  |
| `stores[].name` | string |  |
| `stores[].phoneNumber` | string |  |
| `stores[].postalCode` | string |  |
| `stores[].state` | string |  |
| `stores[].updatedAt` | date | The time when this resource was updated (ISO 8601 format, e.g. 2020-03-30T08:05:10.020Z) |

## Native endpoint

Through the native Loyverse API, this operation is `GET /stores` (base URL `https://api.loyverse.com/v1.0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-stores.md) for the provider-specific parameters and requirements.

