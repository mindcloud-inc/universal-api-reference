# Paradym: List Certificates

Retrieves a list of certificates from Paradym.

```
GET https://connect.mindcloud.co/v1/universal/paradym/latest/actions/list-certificates
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Paradym `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/paradym/latest/actions/list-certificates?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/paradym/latest/actions/list-certificates?${params}`, {
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
| `certificateType` | string | no | Filter certificates by Paradym certificate type. One of: `0`, `1`. |
| `keyType` | string | no | Filter certificates by key type. One of: `0`, `1`. |
| `status` | string | no | Filter certificates by certificate status. One of: `0`, `1`, `2`, `3`, `4`, `5`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": [
        {
          "certificate": "string",
          "createdAt": "string",
          "expiresAt": "string",
          "id": "string",
          "isExternallySigned": true,
          "keyType": "string",
          "status": "string",
          "subjectKeyIdentifier": "string",
          "type": "string",
          "updatedAt": "string"
        }
      ],
      "meta": {
        "filter": {
          "status": "string",
          "type": "string"
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
| `data[].certificate` | string |  |
| `data[].createdAt` | string |  |
| `data[].expiresAt` | string |  |
| `data[].id` | string |  |
| `data[].isExternallySigned` | boolean |  |
| `data[].keyType` | string |  |
| `data[].status` | string |  |
| `data[].subjectKeyIdentifier` | string |  |
| `data[].type` | string |  |
| `data[].updatedAt` | string |  |
| `meta.filter.status` | string |  |
| `meta.filter.type` | string |  |
| `meta.page.maxSize` | string |  |
| `meta.page.size` | string |  |
| `meta.sort[].id` | string |  |

## Native endpoint

Through the native Paradym API, this operation is `GET /projects/:projectId/certificates` (base URL `https://api.paradym.id/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-certificates.md) for the provider-specific parameters and requirements.

