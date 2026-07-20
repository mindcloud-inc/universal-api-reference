# Sipuni: Get Recording

Retrieves a call recording audio file from Sipuni.

```
GET https://connect.mindcloud.co/v1/universal/sipuni/latest/actions/get-recording
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Sipuni `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sipuni/latest/actions/get-recording?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sipuni/latest/actions/get-recording?${params}`, {
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
| `id` | string | yes | Recording ID from the exported statistics CSV. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "response": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `response` | string | Raw recording payload returned by Sipuni. |

## Native endpoint

Through the native Sipuni API, this operation is `GET /statistic/record` (base URL `https://sipuni.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-recording.md) for the provider-specific parameters and requirements.

