# Fingertip: Create Site



```
POST https://connect.mindcloud.co/v1/universal/fingertip/latest/actions/create-site
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Fingertip `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/fingertip/latest/actions/create-site" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen",
  "slug": "string",
  "businessType": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/fingertip/latest/actions/create-site', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Ava Chen",
    "slug": "string",
    "businessType": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | yes | Name of the site |
| `slug` | string | yes | URL-friendly identifier for the site |
| `businessType` | string | yes | Type of business the site represents |
| `description` | string | no | Description of the site |
| `status` | string | no | Current status of the site |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `locationId` | string | no | ID of the associated location |
| `homePageId` | string | no | ID of the site's home page |
| `timeZone` | string | no | Time zone for the site |
| `workspaceId` | string | no | ID of the workspace this site belongs to |

## Response

```json
{
  "success": true,
  "data": [
    {
      "site": {
        "businessType": "string",
        "createdAt": "2026-05-07T12:00:00.000Z",
        "description": "string",
        "homePageId": "string",
        "id": "string",
        "locationId": "string",
        "logoMedia": {},
        "name": "Ava Chen",
        "overridePlan": "string",
        "slug": "string",
        "socialIcons": {},
        "status": "string",
        "timeZone": "string",
        "updatedAt": "2026-05-07T12:00:00.000Z",
        "workspaceId": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `site` | object | The newly created site |
| `site.businessType` | string |  |
| `site.createdAt` | date |  |
| `site.description` | string |  |
| `site.homePageId` | string |  |
| `site.id` | string |  |
| `site.locationId` | string |  |
| `site.logoMedia` | object |  |
| `site.name` | string |  |
| `site.overridePlan` | string |  |
| `site.slug` | string |  |
| `site.socialIcons` | object |  |
| `site.status` | string |  |
| `site.timeZone` | string |  |
| `site.updatedAt` | date |  |
| `site.workspaceId` | string |  |

## Native endpoint

Through the native Fingertip API, this operation is `POST /v1/sites` (base URL `https://api.fingertip.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-site.md) for the provider-specific parameters and requirements.

