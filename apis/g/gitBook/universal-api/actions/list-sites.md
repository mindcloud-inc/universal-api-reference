# GitBook: List Sites

Retrieves sites from a GitBook organization.

```
GET https://connect.mindcloud.co/v1/universal/gitBook/latest/actions/list-sites
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GitBook `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/gitBook/latest/actions/list-sites?connectionId=$CONNECTION_ID&limit=25&offset=0&organizationId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "organizationId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/gitBook/latest/actions/list-sites?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `organizationId` | string | yes |  |
| `published` | boolean | no |  |
| `space` | string | no |  |
| `title` | string | no |  |
| `type[]` | array<string> | no | Accepts multiple values as an array. |

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

Through the native GitBook API, this operation is `GET /orgs/:organizationId/sites` (base URL `https://api.gitbook.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-sites.md) for the provider-specific parameters and requirements.

