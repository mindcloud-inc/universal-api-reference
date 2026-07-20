# Recut URL Shortener: Update Campaign

Updates an existing campaign in Recut URL Shortener.

```
PUT https://connect.mindcloud.co/v1/universal/recutURLShortener/latest/actions/update-campaign
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Recut URL Shortener `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/recutURLShortener/latest/actions/update-campaign" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": 1,
  "name": "Updated Campaign Name"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/recutURLShortener/latest/actions/update-campaign', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": 1,
    "name": "Updated Campaign Name"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | number | yes | Campaign ID. |
| `name` | string | yes | Campaign name. Example: `Updated Campaign Name`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `slug` | string | no | Rotator slug. |
| `public` | boolean | no | Whether the campaign is publicly accessible. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "campaign": "string",
      "error": 1,
      "id": 1,
      "list": "string",
      "public": true,
      "rotator": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `campaign` | string | Campaign name. |
| `error` | number | Recut API error flag. |
| `id` | number | Updated campaign ID. |
| `list` | string | Campaign list URL. |
| `public` | boolean | Whether the campaign is public. |
| `rotator` | string | Rotator URL. |

## Native endpoint

Through the native Recut URL Shortener API, this operation is `PUT /campaign/:id/update` (base URL `https://app.recut.in/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-campaign.md) for the provider-specific parameters and requirements.

