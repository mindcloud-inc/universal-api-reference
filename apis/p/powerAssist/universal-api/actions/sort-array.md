# Power Assist: Sort Array

Sorts an array with Power Assist.

```
GET https://connect.mindcloud.co/v1/universal/powerAssist/latest/actions/sort-array
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Power Assist `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/powerAssist/latest/actions/sort-array?connectionId=$CONNECTION_ID&array%5B%5D=%5Bobject%20Object%5D" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "array[]": "[object Object]"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/powerAssist/latest/actions/sort-array?${params}`, {
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
| `array[]` | array<object> | yes | The array to sort. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "Result": [
        "string"
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `Result` | array<string> | Sorted array values. |

## Native endpoint

Through the native Power Assist API, this operation is `POST /api/array/sort` (base URL `https://power-assist.p.rapidapi.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/sort-array.md) for the provider-specific parameters and requirements.

