# Rossum: Assign Annotation

Assigns assignees to an annotation in Rossum.

```
PUT https://connect.mindcloud.co/v1/universal/rossum/latest/actions/assign-annotation
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Rossum `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/rossum/latest/actions/assign-annotation" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "annotations[]": [
    "string"
  ],
  "assignees[]": [
    "string"
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/rossum/latest/actions/assign-annotation', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "annotations[]": ["string"],
    "assignees[]": ["string"]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `annotations[]` | array<string> | yes | Annotation URLs to assign. |
| `assignees[]` | array<string> | yes | User URLs to assign to the annotation. |
| `noteContent` | string | no | Optional reassignment note. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Rossum API returns.

## Native endpoint

Through the native Rossum API, this operation is `POST /annotations/assign` (base URL `https://mindcloud.rossum.app/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/assign-annotation.md) for the provider-specific parameters and requirements.

