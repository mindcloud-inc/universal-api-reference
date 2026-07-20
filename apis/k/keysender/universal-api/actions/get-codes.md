# Keysender: Get Codes

Retrieves codes from Keysender.

```
GET https://connect.mindcloud.co/v1/universal/keysender/latest/actions/get-codes
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Keysender `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/keysender/latest/actions/get-codes?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/keysender/latest/actions/get-codes?${params}`, {
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
| `databaseId` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "filename": "Ava Chen",
      "id": 1,
      "keyusage": 1,
      "sendfirst": 1,
      "status": 1,
      "type": 1,
      "value": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `filename` | string | Stored filename for file codes. |
| `id` | number | Code identifier. |
| `keyusage` | number | Usage count. |
| `sendfirst` | number | Send-first flag. |
| `status` | number | Code usage status. |
| `type` | number | Code type. |
| `value` | string | Code value or filename. |

## Native endpoint

Through the native Keysender API, this operation is `GET /codes` (base URL `https://panel.keysender.co.uk/api/v1.0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-codes.md) for the provider-specific parameters and requirements.

