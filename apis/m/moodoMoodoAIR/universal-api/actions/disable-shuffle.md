# Moodo & Moodo AIR: Disable Shuffle

Disables shuffle mode on a Moodo box.

```
DELETE https://connect.mindcloud.co/v1/universal/moodoMoodoAIR/latest/actions/disable-shuffle
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Moodo & Moodo AIR `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/moodoMoodoAIR/latest/actions/disable-shuffle?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/moodoMoodoAIR/latest/actions/disable-shuffle?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



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

Through the native Moodo & Moodo AIR API, this operation is `DELETE /shuffle/:device_key` (base URL `https://rest.moodo.co/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/disable-shuffle.md) for the provider-specific parameters and requirements.

