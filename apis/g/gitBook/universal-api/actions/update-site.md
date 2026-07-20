# GitBook: Update Site

Updates an existing site in GitBook.

```
PUT https://connect.mindcloud.co/v1/universal/gitBook/latest/actions/update-site
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GitBook `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/gitBook/latest/actions/update-site" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "organizationId": "string",
  "siteId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/gitBook/latest/actions/update-site', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "organizationId": "string",
    "siteId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `basename` | string | no |  |
| `defaultLevel` | string | no | Default level applied to the site. |
| `defaultSiteSection` | string | no |  |
| `defaultSiteSpace` | string | no |  |
| `organizationId` | string | yes |  |
| `permissionsModel` | string | no |  |
| `siteId` | string | yes |  |
| `title` | string | no | Title of the site. |
| `visibility` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "appliedType": "string",
      "basename": "Ava Chen",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "defaultLevel": "string",
      "id": "string",
      "object": "string",
      "permissionsModel": "string",
      "published": true,
      "siteSpaces": 1,
      "title": "string",
      "type": "string",
      "urls": {
        "app": "https://example.com",
        "location": "https://example.com",
        "preview": "https://example.com"
      },
      "visibility": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `appliedType` | string |  |
| `basename` | string |  |
| `createdAt` | date |  |
| `defaultLevel` | string |  |
| `id` | string |  |
| `object` | string |  |
| `permissionsModel` | string |  |
| `published` | boolean |  |
| `siteSpaces` | number |  |
| `title` | string |  |
| `type` | string |  |
| `urls.app` | string |  |
| `urls.location` | string |  |
| `urls.preview` | string |  |
| `visibility` | string |  |

## Native endpoint

Through the native GitBook API, this operation is `PATCH /orgs/:organizationId/sites/:siteId` (base URL `https://api.gitbook.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-site.md) for the provider-specific parameters and requirements.

