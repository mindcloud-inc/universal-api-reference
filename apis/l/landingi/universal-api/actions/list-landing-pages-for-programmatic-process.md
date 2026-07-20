# Landingi: List Landing Pages for Programmatic Process

Retrieves landing pages for a Landingi programmatic process.

```
GET https://connect.mindcloud.co/v1/universal/landingi/latest/actions/list-landing-pages-for-programmatic-process
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Landingi `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/landingi/latest/actions/list-landing-pages-for-programmatic-process?connectionId=$CONNECTION_ID&limit=25&offset=0&processUuid=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "processUuid": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/landingi/latest/actions/list-landing-pages-for-programmatic-process?${params}`, {
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
| `processUuid` | string | yes | Programmatic process UUID. |
| `filters` | object | no |  |
| `filters.query` | string | no | Search by landing page name or assigned URL. |
| `filters.status` | string | no | Filter by landing page status. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "archived": true,
      "identifier": "string",
      "name": "Ava Chen",
      "published": true,
      "status": "string",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `archived` | boolean | Whether the landing page is archived. |
| `identifier` | string | Landing page identifier. |
| `name` | string | Landing page name. |
| `published` | boolean | Whether the landing page is published. |
| `status` | string | Current landing page status. |
| `url` | string | Landing page URL. |

## Native endpoint

Through the native Landingi API, this operation is `GET /landing-page/programmatic/processes/:processUuid/landing-pages` (base URL `https://api.landingi.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-landing-pages-for-programmatic-process.md) for the provider-specific parameters and requirements.

