# Paradym: List Issued Credentials

Retrieves issued credentials from Paradym.

```
GET https://connect.mindcloud.co/v1/universal/paradym/latest/actions/list-issued-credentials
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Paradym `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/paradym/latest/actions/list-issued-credentials?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/paradym/latest/actions/list-issued-credentials?${params}`, {
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
| `filter[credentialTemplateId]` | string | no |  |
| `filter[status]` | string | no |  |
| `filter[exchange]` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": [
        {
          "credentialTemplateId": "string",
          "exchange": "string",
          "format": "string",
          "id": "string",
          "revocable": true,
          "status": "string"
        }
      ],
      "meta": {
        "filter": {
          "credentialTemplateId": "string"
        },
        "page": {
          "maxSize": "string",
          "size": "string"
        },
        "sort": [
          {
            "id": "string"
          }
        ]
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data[].credentialTemplateId` | string |  |
| `data[].exchange` | string |  |
| `data[].format` | string |  |
| `data[].id` | string |  |
| `data[].revocable` | boolean |  |
| `data[].status` | string |  |
| `meta.filter.credentialTemplateId` | string |  |
| `meta.page.maxSize` | string |  |
| `meta.page.size` | string |  |
| `meta.sort[].id` | string |  |

## Native endpoint

Through the native Paradym API, this operation is `GET /projects/:projectId/issuance` (base URL `https://api.paradym.id/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-issued-credentials.md) for the provider-specific parameters and requirements.

