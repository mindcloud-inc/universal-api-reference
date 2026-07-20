# Convertio: Delete Conversion

Deletes or cancels a conversion from Convertio.

```
DELETE https://connect.mindcloud.co/v1/universal/convertio/latest/actions/delete-conversion
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Convertio `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/convertio/latest/actions/delete-conversion?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/convertio/latest/actions/delete-conversion?${params}`, {
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
| `id` | string | yes | Conversion ID returned by Start Conversion. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "code": 1,
      "data": {},
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `code` | number |  |
| `data` | object |  |
| `status` | string |  |

## Native endpoint

Through the native Convertio API, this operation is `DELETE /convert/:id` (base URL `https://api.convertio.co`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-conversion.md) for the provider-specific parameters and requirements.

