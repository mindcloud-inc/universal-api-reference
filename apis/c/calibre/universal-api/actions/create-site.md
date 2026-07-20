# Calibre: Create Site

Creates a new site in Calibre.

```
POST https://connect.mindcloud.co/v1/universal/calibre/latest/actions/create-site
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Calibre `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/calibre/latest/actions/create-site" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "variables.siteName": "Ava Chen",
  "variables.team": "string",
  "variables.canonicalUrl": "https://example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/calibre/latest/actions/create-site', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "variables.siteName": "Ava Chen",
    "variables.team": "string",
    "variables.canonicalUrl": "https://example.com"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `variables.siteName` | string | yes | Name of the Calibre site to create. |
| `variables.team` | string | yes | Team slug that will own the new site. |
| `variables.location` | string | no | Primary test location for the new site. Default: `NorthVirginia`. |
| `variables.canonicalUrl` | string | yes | Canonical URL for the site. |
| `variables.pageName` | string | no | Name of the initial page added to the site. Default: `Home`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createSite": {
        "canonicalUrl": "https://example.com",
        "name": "Ava Chen",
        "secret": "string",
        "slug": "string",
        "team": {
          "name": "Ava Chen",
          "slug": "string"
        }
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createSite.canonicalUrl` | string |  |
| `createSite.name` | string |  |
| `createSite.secret` | string |  |
| `createSite.slug` | string |  |
| `createSite.team.name` | string |  |
| `createSite.team.slug` | string |  |

## Native endpoint

Through the native Calibre API, this operation is `POST /graphql` (base URL `https://api.calibreapp.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-site.md) for the provider-specific parameters and requirements.

