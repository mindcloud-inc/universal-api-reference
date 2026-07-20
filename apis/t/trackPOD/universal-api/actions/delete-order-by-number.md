# Track-POD: Delete Order By Number

Deletes an existing order from Track-POD by number.

```
DELETE https://connect.mindcloud.co/v1/universal/trackPOD/latest/actions/delete-order-by-number
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Track-POD `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/trackPOD/latest/actions/delete-order-by-number?connectionId=$CONNECTION_ID&number=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "number": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/trackPOD/latest/actions/delete-order-by-number?${params}`, {
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
| `number` | string | yes | Order number |

## Response

```json
{
  "success": true,
  "data": [
    {
      "Detail": "string",
      "Status": 1,
      "Title": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `Detail` | string | A human-readable explanation specific to this response. |
| `Status` | number | The HTTP status code for the response |
| `Title` | string | A short, human-readable summary of the response |

## Native endpoint

Through the native Track-POD API, this operation is `DELETE /Order/Number/:number` (base URL `https://api.track-pod.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-order-by-number.md) for the provider-specific parameters and requirements.

