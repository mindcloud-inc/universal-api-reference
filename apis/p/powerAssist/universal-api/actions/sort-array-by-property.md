# Power Assist: Sort Array By Property

Sorts an array by property with Power Assist.

```
GET https://connect.mindcloud.co/v1/universal/powerAssist/latest/actions/sort-array-by-property
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Power Assist `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/powerAssist/latest/actions/sort-array-by-property?connectionId=$CONNECTION_ID&array%5B%5D=%5Bobject%20Object%5D&propertyName=Ava%20Chen" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "array[]": "[object Object]",
  "propertyName": "Ava Chen"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/powerAssist/latest/actions/sort-array-by-property?${params}`, {
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
| `array[]` | array<object> | yes | Array of objects to sort. |
| `propertyName` | string | yes | Object property to sort by. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `descending` | boolean | no | Whether to sort in descending order. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "Result": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `Result` | array<object> | Objects sorted by the selected property. |

## Native endpoint

Through the native Power Assist API, this operation is `POST /api/array/sortByProperty` (base URL `https://power-assist.p.rapidapi.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/sort-array-by-property.md) for the provider-specific parameters and requirements.

