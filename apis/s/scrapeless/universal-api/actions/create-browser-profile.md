# Scrapeless: Create Browser Profile

Creates a new browser profile in Scrapeless.

```
POST https://connect.mindcloud.co/v1/universal/scrapeless/latest/actions/create-browser-profile
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Scrapeless `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/scrapeless/latest/actions/create-browser-profile" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/scrapeless/latest/actions/create-browser-profile', {
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
| `name` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "name": "Ava Chen",
      "profileId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `name` | string | profile name |
| `profileId` | string | profile id |

## Native endpoint

Through the native Scrapeless API, this operation is `POST /browser/profiles` (base URL `https://api.scrapeless.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-browser-profile.md) for the provider-specific parameters and requirements.

