# Ticketmaster: Get Sub-Genre

Retrieves details for a specific sub-genre from Ticketmaster.

```
GET https://connect.mindcloud.co/v1/universal/ticketmaster/latest/actions/get-sub-genre
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Ticketmaster `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ticketmaster/latest/actions/get-sub-genre?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/ticketmaster/latest/actions/get-sub-genre?${params}`, {
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
| `id` | string | yes | The unique identifier for the sub-genre. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "locale": "string",
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string |  |
| `locale` | string |  |
| `name` | string |  |

## Native endpoint

Through the native Ticketmaster API, this operation is `GET /discovery/v2/classifications/subgenres/:id` (base URL `https://app.ticketmaster.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-sub-genre.md) for the provider-specific parameters and requirements.

