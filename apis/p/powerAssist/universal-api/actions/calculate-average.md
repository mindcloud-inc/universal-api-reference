# Power Assist: Calculate Average

Calculates an average with Power Assist.

```
GET https://connect.mindcloud.co/v1/universal/powerAssist/latest/actions/calculate-average
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Power Assist `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/powerAssist/latest/actions/calculate-average?connectionId=$CONNECTION_ID&numbers%5B%5D=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "numbers[]": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/powerAssist/latest/actions/calculate-average?${params}`, {
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
| `numbers[]` | array<number> | yes | Array of numbers to average. Numeric strings are allowed when they do not contain formatting such as commas. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "Result": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `Result` | number | Average value. |

## Native endpoint

Through the native Power Assist API, this operation is `POST /api/math/average` (base URL `https://power-assist.p.rapidapi.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/calculate-average.md) for the provider-specific parameters and requirements.

