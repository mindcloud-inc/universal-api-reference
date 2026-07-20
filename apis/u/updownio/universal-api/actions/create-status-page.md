# updown.io: Create Status Page

Creates a new status page in updown.io.

```
POST https://connect.mindcloud.co/v1/universal/updownio/latest/actions/create-status-page
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a updown.io `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/updownio/latest/actions/create-status-page" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "checks[]": [
    "string"
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/updownio/latest/actions/create-status-page', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "checks[]": ["string"]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `accessKey` | string | no | Access key for protected pages. |
| `checks[]` | array<string> | yes | List of check tokens to show on the status page. Accepts multiple values as an array. |
| `description` | string | no | Description text displayed below the status page name. |
| `name` | string | no | Name of the status page. |
| `visibility` | list | no | Page visibility: public, protected, or private. One of: `private`, `protected`, `public`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "access_key": "string",
      "checks": [
        "string"
      ],
      "description": "string",
      "name": "Ava Chen",
      "token": "string",
      "url": "https://example.com",
      "visibility": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `access_key` | string | Protected-page access key. |
| `checks` | array<string> | Check tokens shown on the page. |
| `description` | string | Status page description. |
| `name` | string | Status page name. |
| `token` | string | Status page token. |
| `url` | string | Public status page URL. |
| `visibility` | string | Status page visibility. |

## Native endpoint

Through the native updown.io API, this operation is `POST /status_pages` (base URL `https://updown.io/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-status-page.md) for the provider-specific parameters and requirements.

