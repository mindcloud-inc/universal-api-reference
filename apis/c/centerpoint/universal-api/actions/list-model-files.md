# Centerpoint: List Model Files



```
GET https://connect.mindcloud.co/v1/universal/centerpoint/latest/actions/list-model-files
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Centerpoint `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [filtering](../filtering.md) (`where`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/centerpoint/latest/actions/list-model-files?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/centerpoint/latest/actions/list-model-files?${params}`, {
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
| `filter[subjectId]` | number | no |  |
| `filter[subjectType]` | string | no |  |
| `filter[tag]` | string | no | Default: `Photos`. |
| `sort` | string | no | Default: `-createdAt`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `fields[profiles]` | string | no |  |
| `fields[employees]` | string | no |  |
| `fields[buildingDivisions]` | string | no |  |
| `include` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "attributes": {
        "archivedAt": {},
        "createdAt": "string",
        "deletedAt": {},
        "pinToTop": true,
        "subjectId": 1,
        "subjectType": "string",
        "updatedAt": "string"
      },
      "id": "string",
      "relationships": {
        "file": {
          "data": {
            "id": "string",
            "type": "string"
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
| `attributes.archivedAt` | object |  |
| `attributes.createdAt` | string |  |
| `attributes.deletedAt` | object |  |
| `attributes.pinToTop` | boolean |  |
| `attributes.subjectId` | number |  |
| `attributes.subjectType` | string |  |
| `attributes.updatedAt` | string |  |
| `id` | string |  |
| `relationships.file.data.id` | string |  |
| `relationships.file.data.type` | string |  |
| `type` | string |  |

## Native endpoint

Through the native Centerpoint API, this operation is `GET model_files` (base URL `https://api.centerpointconnect.io/centerpoint/`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-model-files.md) for the provider-specific parameters and requirements.

