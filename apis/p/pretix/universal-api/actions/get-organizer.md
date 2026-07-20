# pretix: Get Organizer

Retrieves an organizer from pretix.

```
GET https://connect.mindcloud.co/v1/universal/pretix/latest/actions/get-organizer
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a pretix `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pretix/latest/actions/get-organizer?connectionId=$CONNECTION_ID&organizer=mindcloud-stage0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "organizer": "mindcloud-stage0"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pretix/latest/actions/get-organizer?${params}`, {
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
| `organizer` | string | yes | pretix organizer slug. Example: `mindcloud-stage0`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "name": "Ava Chen",
      "plugins": [
        "string"
      ],
      "publicUrl": "https://example.com",
      "slug": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `name` | string |  |
| `plugins[]` | string |  |
| `publicUrl` | string |  |
| `slug` | string |  |

## Native endpoint

Through the native pretix API, this operation is `GET /organizers/:organizer/` (base URL `https://pretix.eu/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-organizer.md) for the provider-specific parameters and requirements.

