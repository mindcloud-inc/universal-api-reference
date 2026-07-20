# Userback: Delete Workflow

Deletes a workflow from Userback.

```
DELETE https://connect.mindcloud.co/v1/universal/userback/latest/actions/delete-workflow
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Userback `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/userback/latest/actions/delete-workflow?connectionId=$CONNECTION_ID&id=563469" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "563469"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/userback/latest/actions/delete-workflow?${params}`, {
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
| `id` | number | yes | The workflow ID to delete. Example: `563469`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "response": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `response` | boolean |  |

## Native endpoint

Through the native Userback API, this operation is `DELETE /workflow/:id` (base URL `https://rest.userback.io/1.0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-workflow.md) for the provider-specific parameters and requirements.

