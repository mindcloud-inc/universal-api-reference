# Loqate: Find UK Location

Finds a UK location with Loqate.

```
GET https://connect.mindcloud.co/v1/universal/loqate/latest/actions/find-uk-location
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Loqate `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/loqate/latest/actions/find-uk-location?connectionId=$CONNECTION_ID&location=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "location": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/loqate/latest/actions/find-uk-location?${params}`, {
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
| `location` | string | yes | The UK location to find. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "location": "string",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string |  |
| `location` | string |  |
| `type` | string |  |

## Native endpoint

Through the native Loqate API, this operation is `GET /Geocoding/UK/Find/v2.00/json6.ws` (base URL `https://api.addressy.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/find-uk-location.md) for the provider-specific parameters and requirements.

