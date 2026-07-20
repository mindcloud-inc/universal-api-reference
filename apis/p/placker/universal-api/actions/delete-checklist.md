# Placker: Delete Checklist



```
DELETE https://connect.mindcloud.co/v1/universal/placker/latest/actions/delete-checklist
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Placker `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/placker/latest/actions/delete-checklist?connectionId=$CONNECTION_ID&checklist=sjwa8k5le5p1c" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "checklist": "sjwa8k5le5p1c"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/placker/latest/actions/delete-checklist?${params}`, {
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
| `checklist` | string | yes | Checklist ID. Example: `sjwa8k5le5p1c`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `status` | string | Operation status. |

## Native endpoint

Through the native Placker API, this operation is `DELETE /checklist/:checklist` (base URL `https://api.placker.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-checklist.md) for the provider-specific parameters and requirements.

