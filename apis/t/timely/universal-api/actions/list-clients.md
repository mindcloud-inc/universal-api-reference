# Timely: List Clients

Retrieves clients from Timely.

```
GET https://connect.mindcloud.co/v1/universal/timely/latest/actions/list-clients
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Timely `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/timely/latest/actions/list-clients?connectionId=$CONNECTION_ID&accountId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "accountId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/timely/latest/actions/list-clients?${params}`, {
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
| `accountId` | number | yes | Account ID for the clients you want to retrieve |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `limit` | number | no | Retrieve number of clients Default: `10000`. |
| `order` | string | no | "asc (default)" and "desc" Default: `asc`. |
| `offset` | number | no | Retrieve clients from offset Default: `0`. |
| `show` | string | no | Specifies which records to retrieve. Example: "show=all" or "show=active" or "show=archived" |

## Response

```json
{
  "success": true,
  "data": [
    {
      "active": true,
      "color": "string",
      "external_id": "string",
      "external_references": {
        "connection_id": 1,
        "id": 1,
        "provider_id": "string",
        "provider_type": "string",
        "updated_at": "2026-05-07T12:00:00.000Z",
        "url": "https://example.com"
      },
      "id": 1,
      "name": "Ava Chen",
      "tic": {
        "external_url": "https://example.com",
        "tool_id": "string",
        "uri": "string"
      },
      "updated_at": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `active` | boolean |  |
| `color` | string |  |
| `external_id` | string |  |
| `external_references` | array<object> |  |
| `external_references.connection_id` | number |  |
| `external_references.id` | number |  |
| `external_references.provider_id` | string |  |
| `external_references.provider_type` | string |  |
| `external_references.updated_at` | date |  |
| `external_references.url` | string |  |
| `id` | number |  |
| `name` | string |  |
| `tic` | object |  |
| `tic.external_url` | string |  |
| `tic.tool_id` | string |  |
| `tic.uri` | string |  |
| `updated_at` | date |  |

## Native endpoint

Through the native Timely API, this operation is `GET /1.1/{account_id}/clients` (base URL `https://api.timelyapp.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-clients.md) for the provider-specific parameters and requirements.

