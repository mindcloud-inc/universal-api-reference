# CircleCI: Create URL Orb Allow List Entry



```
POST https://connect.mindcloud.co/v1/universal/circleCI/latest/actions/create-url-orb-allow-list-entry
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CircleCI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/circleCI/latest/actions/create-url-orb-allow-list-entry" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "auth": "string",
  "name": "MindCloud Test Entry",
  "orgSlugOrId": "circleci/NheMuBArzQftQimV3Bqqky",
  "prefix": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/circleCI/latest/actions/create-url-orb-allow-list-entry', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "auth": "string",
    "name": "MindCloud Test Entry",
    "orgSlugOrId": "circleci/NheMuBArzQftQimV3Bqqky",
    "prefix": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `auth` | string | yes | The auth mode for fetching matching URL orbs. |
| `name` | string | yes | The allow-list entry name. Default: `MindCloud Test Entry`. |
| `orgSlugOrId` | string | yes | The CircleCI organization slug or ID. Default: `circleci/NheMuBArzQftQimV3Bqqky`. |
| `prefix` | string | yes | The URL prefix to allow. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "message": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string |  |
| `message` | string |  |

## Native endpoint

Through the native CircleCI API, this operation is `POST /organization/:org_slug_or_id/url-orb-allow-list` (base URL `https://circleci.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-url-orb-allow-list-entry.md) for the provider-specific parameters and requirements.

