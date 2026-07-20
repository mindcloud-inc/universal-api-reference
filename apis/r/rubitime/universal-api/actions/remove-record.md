# Rubitime: Remove Record

Deletes an existing record from Rubitime.

```
DELETE https://connect.mindcloud.co/v1/universal/rubitime/latest/actions/remove-record
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Rubitime `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/rubitime/latest/actions/remove-record?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/rubitime/latest/actions/remove-record?${params}`, {
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
| `id` | number | yes | Rubitime record ID to delete. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": [
        {}
      ],
      "message": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | array<object> | Provider result payload returned by Rubitime. |
| `message` | string | Provider message returned by Rubitime for the delete request. |
| `status` | string | Rubitime request status, typically ok or error. |

## Native endpoint

Through the native Rubitime API, this operation is `POST /remove-record` (base URL `https://rubitime.ru/api2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/remove-record.md) for the provider-specific parameters and requirements.

