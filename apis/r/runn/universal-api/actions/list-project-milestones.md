# Runn: List Project Milestones



```
GET https://connect.mindcloud.co/v1/universal/runn/latest/actions/list-project-milestones
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Runn `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/runn/latest/actions/list-project-milestones?connectionId=$CONNECTION_ID&projectId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "projectId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/runn/latest/actions/list-project-milestones?${params}`, {
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
| `projectId` | number | yes | Runn project ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "nextCursor": "string",
      "values": [
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
| `nextCursor` | string | Cursor for the next page of results, or null. |
| `values` | array<object> | Project milestones. |

## Native endpoint

Through the native Runn API, this operation is `GET /projects/{{projectId}}/milestones/` (base URL `https://api.runn.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-project-milestones.md) for the provider-specific parameters and requirements.

