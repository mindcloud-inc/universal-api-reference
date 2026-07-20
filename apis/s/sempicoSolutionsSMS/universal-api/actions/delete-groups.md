# Sempico Solutions SMS: Delete Groups



```
DELETE https://connect.mindcloud.co/v1/universal/sempicoSolutionsSMS/latest/actions/delete-groups
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Sempico Solutions SMS `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/sempicoSolutionsSMS/latest/actions/delete-groups?connectionId=$CONNECTION_ID&id_group%5B%5D=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id_group[]": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sempicoSolutionsSMS/latest/actions/delete-groups?${params}`, {
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
| `id_group[]` | array<number> | yes | Group IDs to delete. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "groupDetails": {
        "command": "string",
        "deleteCount": 1
      },
      "list": [
        1
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `groupDetails.command` | string | Operation performed. |
| `groupDetails.deleteCount` | number | Number of groups deleted. |
| `list` | array<number> | Deleted group IDs. |

## Native endpoint

Through the native Sempico Solutions SMS API, this operation is `POST /group-delete` (base URL `https://restapi.sempico.solutions/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-groups.md) for the provider-specific parameters and requirements.

