# Storyblok: List Links in Folder

Retrieves Storyblok links from a specific folder.

```
GET https://connect.mindcloud.co/v1/universal/storyblok/latest/actions/list-links-in-folder
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Storyblok `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/storyblok/latest/actions/list-links-in-folder?connectionId=$CONNECTION_ID&limit=25&offset=0&startsWith=home" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "startsWith": "home"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/storyblok/latest/actions/list-links-in-folder?${params}`, {
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
| `startsWith` | string | yes | Only return links whose real path starts with this folder path prefix. Default: `home`. |
| `version` | string | no | Whether to read draft or published content. Default: `draft`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "links": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `links` | object | Links in the requested folder keyed by UUID. |

## Native endpoint

Through the native Storyblok API, this operation is `GET /links` (base URL `https://api.storyblok.com/v2/cdn`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-links-in-folder.md) for the provider-specific parameters and requirements.

