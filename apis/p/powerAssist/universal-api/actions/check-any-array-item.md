# Power Assist: Check Any Array Item

Checks whether any array item matches in Power Assist.

```
GET https://connect.mindcloud.co/v1/universal/powerAssist/latest/actions/check-any-array-item
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Power Assist `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/powerAssist/latest/actions/check-any-array-item?connectionId=$CONNECTION_ID&array%5B%5D=%5Bobject%20Object%5D&propertyName=Ava%20Chen&comparison=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "array[]": "[object Object]",
  "propertyName": "Ava Chen",
  "comparison": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/powerAssist/latest/actions/check-any-array-item?${params}`, {
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
| `array[]` | array<object> | yes | Array of items to test. |
| `propertyName` | string | yes | Use this for simple values, or the object property to compare. |
| `comparison` | string | yes | Comparison operation to apply. |
| `value` | string | no | Value to compare against. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `valueType` | string | no | Optional type of the comparison value. If blank, the value is treated as a string. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "Result": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `Result` | boolean | Whether any item matched. |

## Native endpoint

Through the native Power Assist API, this operation is `POST /api/array/any` (base URL `https://power-assist.p.rapidapi.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/check-any-array-item.md) for the provider-specific parameters and requirements.

