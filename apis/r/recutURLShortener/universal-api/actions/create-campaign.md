# Recut URL Shortener: Create Campaign

Creates a campaign in Recut URL Shortener.

```
POST https://connect.mindcloud.co/v1/universal/recutURLShortener/latest/actions/create-campaign
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Recut URL Shortener `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/recutURLShortener/latest/actions/create-campaign" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Codex Stage 3 Campaign"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/recutURLShortener/latest/actions/create-campaign', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Codex Stage 3 Campaign"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | yes | Campaign name. Example: `Codex Stage 3 Campaign`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `slug` | string | no | Rotator slug. Example: `codex-stage-3-campaign`. |
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
| `id` | number | Created campaign ID. |
| `list` | string | Campaign list URL. |
| `public` | boolean | Whether the campaign is public. |
| `rotator` | string | Campaign rotator URL. |

## Native endpoint

Through the native Recut URL Shortener API, this operation is `POST /campaign/add` (base URL `https://app.recut.in/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-campaign.md) for the provider-specific parameters and requirements.

