# Passslot: Delete Scanner



```
DELETE https://connect.mindcloud.co/v1/universal/passslot/latest/actions/delete-scanner
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Passslot `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/passslot/latest/actions/delete-scanner?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/passslot/latest/actions/delete-scanner?${params}`, {
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
| `id` | string | yes | Passslot scanner ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "deleted": true,
      "id": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `deleted` | boolean | Whether the scanner was deleted. |
| `id` | string | Deleted scanner ID. |

## Native endpoint

Through the native Passslot API, this operation is `DELETE scanners/:id` (base URL `https://api.passslot.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-scanner.md) for the provider-specific parameters and requirements.

