# Encodian - Utilities: Utilities - Array Add Items



```
GET https://connect.mindcloud.co/v1/universal/encodianUtilities/latest/actions/utilities-array-add-items
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Encodian - Utilities `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/encodianUtilities/latest/actions/utilities-array-add-items?connectionId=$CONNECTION_ID&data=string&items=string&itemPosition=Last" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "data": "string",
  "items": "string",
  "itemPosition": "Last"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/encodianUtilities/latest/actions/utilities-array-add-items?${params}`, {
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
| `data` | string | yes | The JSON array or object to modify |
| `items` | string | yes | The items to add to the 'Data' provided |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `itemPosition` | string | yes | Set whether to return the first item, last item or a specified item One of: `0`, `1`, `2`. Default: `Last`. |
| `itemIndex` | number | no | Index of the item to return. This is only applicable when the 'Item Position' property is set to 'Specific' |
| `path` | string | no | Select a specific node within the 'Data' using a JSONPath expression |

## Response

```json
{
  "success": true,
  "data": [
    {
      "errors": [
        "string"
      ],
      "httpStatusCode": 1,
      "httpStatusMessage": "string",
      "operationId": "string",
      "operationStatus": "string",
      "result": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `errors` | array<string> |  |
| `httpStatusCode` | number |  |
| `httpStatusMessage` | string |  |
| `operationId` | string |  |
| `operationStatus` | string |  |
| `result` | string | The response value for the request |

## Native endpoint

Through the native Encodian - Utilities API, this operation is `POST /api/v1/Utilities/ArrayAddItems` (base URL `https://api.apps-encodian.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/utilities-array-add-items.md) for the provider-specific parameters and requirements.

