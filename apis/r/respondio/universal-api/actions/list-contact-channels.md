# respond.io: List Contact Channels

Retrieves contact channels from respond.io.

```
GET https://connect.mindcloud.co/v1/universal/respondio/latest/actions/list-contact-channels
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a respond.io `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/respondio/latest/actions/list-contact-channels?connectionId=$CONNECTION_ID&limit=25&offset=0&identifier=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "identifier": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/respondio/latest/actions/list-contact-channels?${params}`, {
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
| `identifier` | string | yes | Contact identifier (id:, email:, or phone:). |

## Response

```json
{
  "success": true,
  "data": [
    {
      "items": {},
      "pagination": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `items` | object |  |
| `pagination` | object |  |

## Native endpoint

Through the native respond.io API, this operation is `GET /contact/:identifier/channels` (base URL `https://api.respond.io/v2`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-contact-channels.md) for the provider-specific parameters and requirements.

