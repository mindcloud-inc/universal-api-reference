# Elastic Cloud: Search Deployments

Finds deployments in Elastic Cloud by query.

```
GET https://connect.mindcloud.co/v1/universal/elasticCloud/latest/actions/search-deployments
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Elastic Cloud `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/elasticCloud/latest/actions/search-deployments?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/elasticCloud/latest/actions/search-deployments?${params}`, {
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
| `body` | object | no | Optional search query for deployment search. |
| `minimalMetadata` | string | no | Comma-separated deployment attributes to include in the minimal metadata response. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "cursor": "string",
      "deployments": [
        {
          "healthy": true,
          "id": "string",
          "metadata": {
            "hidden": true,
            "organizationId": "string",
            "systemOwned": true
          },
          "name": "Ava Chen",
          "settings": {
            "solutionType": "string"
          }
        }
      ],
      "matchCount": 1,
      "returnCount": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `cursor` | string |  |
| `deployments[].healthy` | boolean |  |
| `deployments[].id` | string |  |
| `deployments[].metadata.hidden` | boolean |  |
| `deployments[].metadata.organizationId` | string |  |
| `deployments[].metadata.systemOwned` | boolean |  |
| `deployments[].name` | string |  |
| `deployments[].settings.solutionType` | string |  |
| `matchCount` | number |  |
| `returnCount` | number |  |

## Native endpoint

Through the native Elastic Cloud API, this operation is `POST /deployments/_search` (base URL `https://api.elastic-cloud.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-deployments.md) for the provider-specific parameters and requirements.

