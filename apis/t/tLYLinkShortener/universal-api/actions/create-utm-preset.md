# TLY Link Shortener: Create UTM Preset

Creates a new UTM preset in TLY Link Shortener.

```
POST https://connect.mindcloud.co/v1/universal/tLYLinkShortener/latest/actions/create-utm-preset
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a TLY Link Shortener `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/tLYLinkShortener/latest/actions/create-utm-preset" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/tLYLinkShortener/latest/actions/create-utm-preset', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | yes | The preset name. |
| `source` | string | no | Optional UTM source value. |
| `medium` | string | no | Optional UTM medium value. |
| `campaign` | string | no | Optional UTM campaign value. |
| `content` | string | no | Optional UTM content value. |
| `term` | string | no | Optional UTM term value. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "campaign": "string",
      "content": "string",
      "created_at": "2026-05-07T12:00:00.000Z",
      "id": 1,
      "medium": "string",
      "name": "Ava Chen",
      "source": "string",
      "term": "string",
      "updated_at": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `campaign` | string |  |
| `content` | string |  |
| `created_at` | date |  |
| `id` | number |  |
| `medium` | string |  |
| `name` | string |  |
| `source` | string |  |
| `term` | string |  |
| `updated_at` | date |  |

## Native endpoint

Through the native TLY Link Shortener API, this operation is `POST /api/v1/link/utm-preset` (base URL `https://api.t.ly`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-utm-preset.md) for the provider-specific parameters and requirements.

