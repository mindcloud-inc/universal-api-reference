# Calibre: List Deploys

Retrieves deploys for a site from Calibre.

```
GET https://connect.mindcloud.co/v1/universal/calibre/latest/actions/list-deploys
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Calibre `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/calibre/latest/actions/list-deploys?connectionId=$CONNECTION_ID&variables.site=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "variables.site": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/calibre/latest/actions/list-deploys?${params}`, {
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
| `variables.site` | string | yes | Site slug, found in site settings. |
| `variables.first` | number | no | Maximum number of deploys to return. Default: `20`. |
| `variables.from` | string | no | Lower bound ISO8601 date filter for deploys. |
| `variables.to` | string | no | Upper bound ISO8601 date filter for deploys. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "organisation": {
        "site": {
          "deploys": {
            "nodes": [
              {
                "createdAt": "2026-05-07T12:00:00.000Z",
                "repository": "string",
                "revision": "string",
                "url": "https://example.com",
                "username": "Ava Chen",
                "uuid": "string"
              }
            ],
            "pageInfo": {
              "endCursor": "string",
              "hasNextPage": true,
              "hasPreviousPage": true,
              "startCursor": "string"
            }
          }
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
| `organisation.site.deploys.nodes[].createdAt` | date |  |
| `organisation.site.deploys.nodes[].repository` | string |  |
| `organisation.site.deploys.nodes[].revision` | string |  |
| `organisation.site.deploys.nodes[].url` | string |  |
| `organisation.site.deploys.nodes[].username` | string |  |
| `organisation.site.deploys.nodes[].uuid` | string |  |
| `organisation.site.deploys.pageInfo.endCursor` | string |  |
| `organisation.site.deploys.pageInfo.hasNextPage` | boolean |  |
| `organisation.site.deploys.pageInfo.hasPreviousPage` | boolean |  |
| `organisation.site.deploys.pageInfo.startCursor` | string |  |

## Native endpoint

Through the native Calibre API, this operation is `POST /graphql` (base URL `https://api.calibreapp.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-deploys.md) for the provider-specific parameters and requirements.

