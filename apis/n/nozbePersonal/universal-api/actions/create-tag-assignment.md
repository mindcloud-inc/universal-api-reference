# Nozbe Personal: Create Tag Assignment

Creates a new tag assignment in Nozbe Personal.

```
POST https://connect.mindcloud.co/v1/universal/nozbePersonal/latest/actions/create-tag-assignment
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Nozbe Personal `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/nozbePersonal/latest/actions/create-tag-assignment" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "tagId": "WjCQV1u7QtKuXhnT",
  "taskId": "Sh2usER2pcbcOtWT"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/nozbePersonal/latest/actions/create-tag-assignment', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "tagId": "WjCQV1u7QtKuXhnT",
    "taskId": "Sh2usER2pcbcOtWT"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `tagId` | string | yes | Tag to assign. Example: `WjCQV1u7QtKuXhnT`. |
| `taskId` | string | yes | Task that receives the tag. Example: `Sh2usER2pcbcOtWT`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "tagId": "string",
      "taskId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string |  |
| `tagId` | string |  |
| `taskId` | string |  |

## Native endpoint

Through the native Nozbe Personal API, this operation is `POST /tag_assignments` (base URL `https://api4.nozbe.com/v1/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-tag-assignment.md) for the provider-specific parameters and requirements.

