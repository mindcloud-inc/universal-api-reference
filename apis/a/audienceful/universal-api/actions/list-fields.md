# Audienceful: List Fields

Retrieves a list of custom fields from Audienceful.

```
GET https://connect.mindcloud.co/v1/universal/audienceful/latest/actions/list-fields
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Audienceful `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/audienceful/latest/actions/list-fields?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/audienceful/latest/actions/list-fields?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "dataName": "Ava Chen",
      "editable": true,
      "id": "string",
      "internal": true,
      "name": "Ava Chen",
      "required": true,
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `dataName` | string |  |
| `editable` | boolean |  |
| `id` | string |  |
| `internal` | boolean |  |
| `name` | string |  |
| `required` | boolean |  |
| `type` | string |  |

## Native endpoint

Through the native Audienceful API, this operation is `GET /people/fields/` (base URL `https://app.audienceful.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-fields.md) for the provider-specific parameters and requirements.

