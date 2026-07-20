# JmpTo: Get Link

Retrieves a link from JmpTo.

```
GET https://connect.mindcloud.co/v1/universal/jmpTo/latest/actions/get-link
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a JmpTo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/jmpTo/latest/actions/get-link?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/jmpTo/latest/actions/get-link?${params}`, {
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
| `id` | number | yes | Link ID to retrieve. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "alias": "string",
      "date": "string",
      "description": "string",
      "device": "string",
      "expiry": "string",
      "id": 1,
      "location": "string",
      "longurl": "https://example.com",
      "shorturl": "https://example.com",
      "title": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `alias` | string | Custom short-link alias. |
| `date` | string | Link creation date/time. |
| `description` | string | Resolved page description. |
| `device` | string | Link device-targeting value when set. |
| `expiry` | string | Link expiration value when set. |
| `id` | number | Link ID. |
| `location` | string | Link geo-targeting value when set. |
| `longurl` | string | Destination URL. |
| `shorturl` | string | Shortened URL. |
| `title` | string | Resolved page title. |

## Native endpoint

Through the native JmpTo API, this operation is `GET /url/:id` (base URL `https://jmpto.net/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-link.md) for the provider-specific parameters and requirements.

