# Loqate: Find Addresses

Finds addresses in Loqate by search text.

```
GET https://connect.mindcloud.co/v1/universal/loqate/latest/actions/find-addresses
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Loqate `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/loqate/latest/actions/find-addresses?connectionId=$CONNECTION_ID&text=Loqate" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "text": "Loqate"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/loqate/latest/actions/find-addresses?${params}`, {
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
| `text` | string | yes | Search text used to find matching addresses and places. Example: `Loqate`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "description": "string",
      "highlight": "string",
      "id": "string",
      "text": "string",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `description` | string |  |
| `highlight` | string |  |
| `id` | string |  |
| `text` | string |  |
| `type` | string |  |

## Native endpoint

Through the native Loqate API, this operation is `GET /Capture/Interactive/Find/v1.20/json6.ws` (base URL `https://api.addressy.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/find-addresses.md) for the provider-specific parameters and requirements.

