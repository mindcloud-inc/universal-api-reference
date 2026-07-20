# RotaCloud: Unpublish Shifts

Unpublishes shifts in RotaCloud.

```
DELETE https://connect.mindcloud.co/v1/universal/rotaCloud/latest/actions/unpublish-shifts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a RotaCloud `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/rotaCloud/latest/actions/unpublish-shifts?connectionId=$CONNECTION_ID&shifts%5B%5D=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "shifts[]": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/rotaCloud/latest/actions/unpublish-shifts?${params}`, {
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
| `shifts[]` | array<number> | yes | Shift IDs to unpublish. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "code": 1,
      "id": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `code` | number |  |
| `id` | number |  |

## Native endpoint

Through the native RotaCloud API, this operation is `DELETE /v1/shifts_published` (base URL `https://api.rotacloud.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/unpublish-shifts.md) for the provider-specific parameters and requirements.

