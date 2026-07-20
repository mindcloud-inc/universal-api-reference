# KiteSuite: Get Project Data

Retrieves all project data from KiteSuite.

```
GET https://connect.mindcloud.co/v1/universal/kiteSuite/latest/actions/get-project-data
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a KiteSuite `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/kiteSuite/latest/actions/get-project-data?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/kiteSuite/latest/actions/get-project-data?${params}`, {
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
| `id` | string | yes | Project ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "docs": [
        {}
      ],
      "epics": [
        {}
      ],
      "itemTypes": [
        {}
      ],
      "lists": [
        {}
      ],
      "project": {},
      "sprints": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `docs` | array<object> |  |
| `epics` | array<object> |  |
| `itemTypes` | array<object> |  |
| `lists` | array<object> |  |
| `project` | object |  |
| `sprints` | array<object> |  |

## Native endpoint

Through the native KiteSuite API, this operation is `GET /api/v1/project/all/:id` (base URL `https://api.kitesuite.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-project-data.md) for the provider-specific parameters and requirements.

