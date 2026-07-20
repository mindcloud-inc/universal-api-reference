# Toodledo: Delete Outlines

Deletes existing outlines from Toodledo.

```
DELETE https://connect.mindcloud.co/v1/universal/toodledo/latest/actions/delete-outlines
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Toodledo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/toodledo/latest/actions/delete-outlines?connectionId=$CONNECTION_ID&outlines=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "outlines": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/toodledo/latest/actions/delete-outlines?${params}`, {
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
| `outlines` | string | yes | JSON-encoded array of outline IDs to delete. |

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
| `id` | string | Deleted outline ID. |

## Native endpoint

Through the native Toodledo API, this operation is `POST /outlines/delete.php` (base URL `https://api.toodledo.com/3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-outlines.md) for the provider-specific parameters and requirements.

