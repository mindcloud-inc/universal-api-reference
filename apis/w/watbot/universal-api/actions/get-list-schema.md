# Watbot: Get List Schema

Retrieves a list schema from Watbot.

```
GET https://connect.mindcloud.co/v1/universal/watbot/latest/actions/get-list-schema
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Watbot `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/watbot/latest/actions/get-list-schema?connectionId=$CONNECTION_ID&schemaId=5dee4800c2cc5a38ec797235" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "schemaId": "5dee4800c2cc5a38ec797235"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/watbot/latest/actions/get-list-schema?${params}`, {
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
| `schemaId` | string | yes | ID of the list schema. Example: `5dee4800c2cc5a38ec797235`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "2026-05-07T12:00:00.000Z",
      "fields": {},
      "id": "string",
      "isMenu": true,
      "name": "Ava Chen",
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | date | List schema creation timestamp. |
| `fields` | object | Field definitions keyed by field slug. |
| `id` | string | List schema ID. |
| `isMenu` | boolean | Whether the list is shown in the Watbot menu. |
| `name` | string | List schema name. |
| `updatedAt` | date | List schema update timestamp. |

## Native endpoint

Through the native Watbot API, this operation is `GET /getListSchema` (base URL `https://watbot.ru/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-list-schema.md) for the provider-specific parameters and requirements.

