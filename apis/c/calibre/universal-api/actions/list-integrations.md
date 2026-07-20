# Calibre: List Integrations

Retrieves integrations for a site from Calibre.

```
GET https://connect.mindcloud.co/v1/universal/calibre/latest/actions/list-integrations
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Calibre `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/calibre/latest/actions/list-integrations?connectionId=$CONNECTION_ID&variables.site=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "variables.site": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/calibre/latest/actions/list-integrations?${params}`, {
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
| `variables.site` | string | yes |  |
| `variables.first` | number | no | Default: `20`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "organisation": {
        "site": {
          "integrationsList": {
            "nodes": [
              {
                "events": [
                  "string"
                ],
                "isDisabled": true,
                "provider": "string",
                "secret": "string",
                "url": "https://example.com",
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
| `organisation.site.integrationsList.nodes[].events[]` | string |  |
| `organisation.site.integrationsList.nodes[].isDisabled` | boolean |  |
| `organisation.site.integrationsList.nodes[].provider` | string |  |
| `organisation.site.integrationsList.nodes[].secret` | string |  |
| `organisation.site.integrationsList.nodes[].url` | string |  |
| `organisation.site.integrationsList.nodes[].uuid` | string |  |
| `organisation.site.integrationsList.pageInfo.endCursor` | string |  |
| `organisation.site.integrationsList.pageInfo.hasNextPage` | boolean |  |
| `organisation.site.integrationsList.pageInfo.hasPreviousPage` | boolean |  |
| `organisation.site.integrationsList.pageInfo.startCursor` | string |  |

## Native endpoint

Through the native Calibre API, this operation is `POST /graphql` (base URL `https://api.calibreapp.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-integrations.md) for the provider-specific parameters and requirements.

