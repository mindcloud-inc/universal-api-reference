# Botbaba: Get Blocks



```
GET https://connect.mindcloud.co/v1/universal/botbaba/latest/actions/get-blocks
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Botbaba `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/botbaba/latest/actions/get-blocks?connectionId=$CONNECTION_ID&botId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "botId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/botbaba/latest/actions/get-blocks?${params}`, {
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
| `botId` | number | yes | The Botbaba bot identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "blockName": "Ava Chen",
      "botId": 1,
      "id": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `blockName` | string |  |
| `botId` | number |  |
| `id` | number |  |

## Native endpoint

Through the native Botbaba API, this operation is `GET /api/GetBlocks` (base URL `https://app.botbaba.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-blocks.md) for the provider-specific parameters and requirements.

