# Moodo & Moodo AIR: Get Box

Retrieves a Moodo box by device key.

```
GET https://connect.mindcloud.co/v1/universal/moodoMoodoAIR/latest/actions/get-box
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Moodo & Moodo AIR `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/moodoMoodoAIR/latest/actions/get-box?connectionId=$CONNECTION_ID&device_key=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "device_key": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/moodoMoodoAIR/latest/actions/get-box?${params}`, {
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
| `device_key` | number | yes | Moodo box device key. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "box": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `box` | object |  |

## Native endpoint

Through the native Moodo & Moodo AIR API, this operation is `GET /boxes/:device_key` (base URL `https://rest.moodo.co/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-box.md) for the provider-specific parameters and requirements.

