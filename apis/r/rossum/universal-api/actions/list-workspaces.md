# Rossum: List Workspaces

Retrieves workspaces from Rossum.

```
GET https://connect.mindcloud.co/v1/universal/rossum/latest/actions/list-workspaces
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Rossum `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/rossum/latest/actions/list-workspaces?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/rossum/latest/actions/list-workspaces?${params}`, {
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
| `name` | string | no | Filter workspaces by name. |
| `ordering` | string | no | Sort workspaces by a supported field using Rossum ordering syntax. |
| `organization` | string | no | Filter workspaces by organization ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "pagination": {
        "next": {},
        "previous": {}
      },
      "results": [
        {
          "autopilot": true,
          "id": 1,
          "modifiedAt": "string",
          "modifiedBy": "string",
          "name": "Ava Chen",
          "organization": "string",
          "queues": [
            "string"
          ],
          "url": "https://example.com"
        }
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `pagination.next` | object |  |
| `pagination.previous` | object |  |
| `results[].autopilot` | boolean |  |
| `results[].id` | number |  |
| `results[].modifiedAt` | string |  |
| `results[].modifiedBy` | string |  |
| `results[].name` | string |  |
| `results[].organization` | string |  |
| `results[].queues[]` | string |  |
| `results[].url` | string |  |

## Native endpoint

Through the native Rossum API, this operation is `GET /workspaces` (base URL `https://mindcloud.rossum.app/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-workspaces.md) for the provider-specific parameters and requirements.

