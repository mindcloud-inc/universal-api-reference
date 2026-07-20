# Salesflare: Get Stage



```
GET https://connect.mindcloud.co/v1/universal/salesflare/latest/actions/get-stage
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Salesflare `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/salesflare/latest/actions/get-stage?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/salesflare/latest/actions/get-stage?${params}`, {
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
| `id` | number | yes | The Salesflare stage ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "fullName": "Ava Chen",
      "id": 1,
      "name": "Ava Chen",
      "order": 1,
      "pipeline": {},
      "probability": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `fullName` | string |  |
| `id` | number |  |
| `name` | string |  |
| `order` | number |  |
| `pipeline` | object |  |
| `probability` | number |  |

## Native endpoint

Through the native Salesflare API, this operation is `GET stages` (base URL `https://api.salesflare.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-stage.md) for the provider-specific parameters and requirements.

