# JmpTo: Create Campaign

Creates a campaign in JmpTo.

```
POST https://connect.mindcloud.co/v1/universal/jmpTo/latest/actions/create-campaign
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a JmpTo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/jmpTo/latest/actions/create-campaign" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/jmpTo/latest/actions/create-campaign', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | no | Campaign name. |
| `slug` | string | no | Rotator slug. |
| `public` | boolean | no | Campaign access flag. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "campaign": "string",
      "error": 1,
      "id": 1,
      "list": "https://example.com",
      "public": true,
      "rotator": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `campaign` | string | Campaign name. |
| `error` | number | Provider success/error code. |
| `id` | number | Campaign ID. |
| `list` | string | Campaign list URL. |
| `public` | boolean | Whether the campaign is public. |
| `rotator` | string | Campaign rotator URL. |

## Native endpoint

Through the native JmpTo API, this operation is `POST /campaign/add` (base URL `https://jmpto.net/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-campaign.md) for the provider-specific parameters and requirements.

