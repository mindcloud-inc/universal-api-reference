# Pingueen: List Clients



```
GET https://connect.mindcloud.co/v1/universal/pingueen/latest/actions/list-clients
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Pingueen `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pingueen/latest/actions/list-clients?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pingueen/latest/actions/list-clients?${params}`, {
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
| `id` | string | no | Filter clients by client ID. |
| `phone` | string | no | Filter clients by phone number. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "_id": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "ds_address": "string",
      "ds_name": "Ava Chen",
      "ds_phone": "string",
      "ds_surname": "Ava Chen",
      "dt_last_message": "2026-05-07T12:00:00.000Z",
      "email": "ava@example.com",
      "is_enabled": true,
      "is_suspended": true,
      "last_message": "string",
      "manual_assignees": [
        {}
      ],
      "meta_info": [
        {}
      ],
      "opt_in": {},
      "read_later": true,
      "user": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `_id` | string |  |
| `createdAt` | date |  |
| `ds_address` | string |  |
| `ds_name` | string |  |
| `ds_phone` | string |  |
| `ds_surname` | string |  |
| `dt_last_message` | date |  |
| `email` | string |  |
| `is_enabled` | boolean |  |
| `is_suspended` | boolean |  |
| `last_message` | string |  |
| `manual_assignees` | array<object> |  |
| `meta_info` | array<object> |  |
| `opt_in` | object |  |
| `read_later` | boolean |  |
| `user` | string |  |

## Native endpoint

Through the native Pingueen API, this operation is `GET /clients` (base URL `https://api.pingueen.it/ext/v2/{{credentials.businessname}}`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-clients.md) for the provider-specific parameters and requirements.

