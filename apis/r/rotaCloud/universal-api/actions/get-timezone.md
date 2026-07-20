# RotaCloud: Get Timezone

Retrieves a timezone from RotaCloud.

```
GET https://connect.mindcloud.co/v1/universal/rotaCloud/latest/actions/get-timezone
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a RotaCloud `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/rotaCloud/latest/actions/get-timezone?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/rotaCloud/latest/actions/get-timezone?${params}`, {
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
| `id` | number | yes | The timezone identifier to retrieve. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "city": "string",
      "continent": "string",
      "id": 1,
      "name": "Ava Chen",
      "sub": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `city` | string |  |
| `continent` | string |  |
| `id` | number |  |
| `name` | string |  |
| `sub` | string |  |

## Native endpoint

Through the native RotaCloud API, this operation is `GET /v1/timezones/:id` (base URL `https://api.rotacloud.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-timezone.md) for the provider-specific parameters and requirements.

