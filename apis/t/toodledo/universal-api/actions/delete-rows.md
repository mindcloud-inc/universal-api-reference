# Toodledo: Delete Rows

Deletes existing rows from Toodledo.

```
DELETE https://connect.mindcloud.co/v1/universal/toodledo/latest/actions/delete-rows
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Toodledo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/toodledo/latest/actions/delete-rows?connectionId=$CONNECTION_ID&rows=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "rows": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/toodledo/latest/actions/delete-rows?${params}`, {
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
| `rows` | string | yes | JSON-encoded array of row delete objects, each containing list and row. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string | Deleted row ID. |

## Native endpoint

Through the native Toodledo API, this operation is `POST /rows/delete.php` (base URL `https://api.toodledo.com/3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-rows.md) for the provider-specific parameters and requirements.

