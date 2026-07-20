# Power Assist: Prepend To Array

Prepends a value to an array with Power Assist.

```
GET https://connect.mindcloud.co/v1/universal/powerAssist/latest/actions/prepend-to-array
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Power Assist `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/powerAssist/latest/actions/prepend-to-array?connectionId=$CONNECTION_ID&array%5B%5D=%5Bobject%20Object%5D&value=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "array[]": "[object Object]",
  "value": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/powerAssist/latest/actions/prepend-to-array?${params}`, {
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
| `array[]` | array<object> | yes | Array to prepend to. |
| `value` | string | yes | Value or array to prepend. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `valueType` | string | no | Optional type of the value. If blank, the value is treated as a string. |

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
| `Result` | array<string> | Array with the new value prepended. |

## Native endpoint

Through the native Power Assist API, this operation is `POST /api/array/prepend` (base URL `https://power-assist.p.rapidapi.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/prepend-to-array.md) for the provider-specific parameters and requirements.

