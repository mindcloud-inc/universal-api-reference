# Raindrop: Remove Multiple Collections



```
DELETE https://connect.mindcloud.co/v1/universal/raindrop/latest/actions/remove-multiple-collections
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Raindrop `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/raindrop/latest/actions/remove-multiple-collections?connectionId=$CONNECTION_ID&ids%5B%5D=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "ids[]": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/raindrop/latest/actions/remove-multiple-collections?${params}`, {
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
| `ids[]` | array<number> | yes | Array of collection IDs to remove. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "ids": [
        1
      ],
      "modified": 1,
      "result": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `ids` | array<number> |  |
| `modified` | number |  |
| `result` | boolean |  |

## Native endpoint

Through the native Raindrop API, this operation is `DELETE /collections` (base URL `https://api.raindrop.io/rest/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/remove-multiple-collections.md) for the provider-specific parameters and requirements.

