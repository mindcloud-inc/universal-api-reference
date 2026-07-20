# TLY Link Shortener: Update UTM Preset

Updates an existing UTM preset in TLY Link Shortener.

```
PUT https://connect.mindcloud.co/v1/universal/tLYLinkShortener/latest/actions/update-utm-preset
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a TLY Link Shortener `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/tLYLinkShortener/latest/actions/update-utm-preset" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": 1,
  "name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/tLYLinkShortener/latest/actions/update-utm-preset', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": 1,
    "name": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | number | yes | The preset ID to update. |
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

Through the native TLY Link Shortener API, this operation is `PUT /api/v1/link/utm-preset/:id` (base URL `https://api.t.ly`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-utm-preset.md) for the provider-specific parameters and requirements.

