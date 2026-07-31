# Random Duck: Get Duck GIF by Number



```
GET https://connect.mindcloud.co/v1/universal/randomDuck/latest/actions/get-duck-gif-by-number
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Random Duck `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/randomDuck/latest/actions/get-duck-gif-by-number?connectionId=$CONNECTION_ID&num=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "num": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/randomDuck/latest/actions/get-duck-gif-by-number?${params}`, {
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
| `num` | number | yes | Required numeric duck GIF filename stem. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": [
        1
      ],
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | array<number> | Native platform Buffer byte sequence for the returned media. |
| `type` | string | Native platform raw-response marker; runtime value is Buffer. |

## Native endpoint

Through the native Random Duck API, this operation is `GET /:num.gif` (base URL `https://random-d.uk/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-duck-gif-by-number.md) for the provider-specific parameters and requirements.

