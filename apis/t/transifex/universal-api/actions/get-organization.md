# Transifex: Get Organization



```
GET https://connect.mindcloud.co/v1/universal/transifex/latest/actions/get-organization
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Transifex `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/transifex/latest/actions/get-organization?connectionId=$CONNECTION_ID&organizationId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "organizationId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/transifex/latest/actions/get-organization?${params}`, {
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
| `organizationId` | string | yes | The Transifex organization identifier, for example o:mindcloud. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "attributes": {
        "name": "Ava Chen",
        "private": true,
        "slug": "string"
      },
      "id": "string",
      "links": {
        "self": "https://example.com"
      },
      "relationships": {
        "projects": {
          "links": {
            "related": "https://example.com"
          }
        },
        "teams": {
          "links": {
            "related": "https://example.com"
          }
        }
      },
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `attributes.name` | string |  |
| `attributes.private` | boolean |  |
| `attributes.slug` | string |  |
| `id` | string |  |
| `links.self` | string |  |
| `relationships.projects.links.related` | string |  |
| `relationships.teams.links.related` | string |  |
| `type` | string |  |

## Native endpoint

Through the native Transifex API, this operation is `GET /organizations/:organization_id` (base URL `https://rest.api.transifex.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-organization.md) for the provider-specific parameters and requirements.

