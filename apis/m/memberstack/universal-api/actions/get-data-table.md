# Memberstack: Get Data Table



```
GET https://connect.mindcloud.co/v1/universal/memberstack/latest/actions/get-data-table
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Memberstack `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/memberstack/latest/actions/get-data-table?connectionId=$CONNECTION_ID&tableKey=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "tableKey": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/memberstack/latest/actions/get-data-table?${params}`, {
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
| `tableKey` | string | yes | Data table key from your Memberstack project. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "2026-05-07T12:00:00.000Z",
      "description": "string",
      "fields": [
        {}
      ],
      "key": "string",
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
| `createdAt` | date |  |
| `description` | string |  |
| `fields` | array<object> |  |
| `key` | string |  |
| `name` | string |  |
| `updatedAt` | date |  |

## Native endpoint

Through the native Memberstack API, this operation is `GET /v2/data-tables/:tableKey` (base URL `https://admin.memberstack.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-data-table.md) for the provider-specific parameters and requirements.

