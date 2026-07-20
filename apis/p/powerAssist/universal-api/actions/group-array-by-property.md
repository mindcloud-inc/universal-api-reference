# Power Assist: Group Array By Property

Groups an array by property with Power Assist.

```
GET https://connect.mindcloud.co/v1/universal/powerAssist/latest/actions/group-array-by-property
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Power Assist `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/powerAssist/latest/actions/group-array-by-property?connectionId=$CONNECTION_ID&array%5B%5D=%5Bobject%20Object%5D" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "array[]": "[object Object]"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/powerAssist/latest/actions/group-array-by-property?${params}`, {
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
| `array[]` | array<object> | yes | Array of items to group. |
| `propertyName` | string | no | Object property to group by. Leave blank for simple values. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "Result": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `Result` | object | Items grouped by property value. |

## Native endpoint

Through the native Power Assist API, this operation is `POST /api/array/groupBy` (base URL `https://power-assist.p.rapidapi.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/group-array-by-property.md) for the provider-specific parameters and requirements.

