# RotaCloud: Delete Availability



```
DELETE https://connect.mindcloud.co/v1/universal/rotaCloud/latest/actions/delete-availability
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a RotaCloud `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/rotaCloud/latest/actions/delete-availability?connectionId=$CONNECTION_ID&user=1&dates%5B%5D=%5Bobject%20Object%5D" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "user": "1",
  "dates[]": "[object Object]"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/rotaCloud/latest/actions/delete-availability?${params}`, {
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
| `user` | number | yes | User ID for the availability deletion. |
| `dates[]` | array<object> | yes | Availability dates to clear. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "deleted": true,
      "id": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `deleted` | boolean |  |
| `id` | number |  |

## Native endpoint

Through the native RotaCloud API, this operation is `POST /v1/availability` (base URL `https://api.rotacloud.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-availability.md) for the provider-specific parameters and requirements.

