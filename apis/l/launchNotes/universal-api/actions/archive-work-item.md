# LaunchNotes: Archive Work Item



```
PUT https://connect.mindcloud.co/v1/universal/launchNotes/latest/actions/archive-work-item
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a LaunchNotes `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/launchNotes/latest/actions/archive-work-item" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "input": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/launchNotes/latest/actions/archive-work-item', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "input": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `input` | object | yes | JSON object matching ArchiveWorkItemInput. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "clientMutationId": "string",
      "errors": [
        {}
      ],
      "workItem": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `clientMutationId` | string | Client mutation identifier. |
| `errors` | array<object> | User errors returned by LaunchNotes. |
| `workItem` | object | Archived work item object. |

## Native endpoint

Through the native LaunchNotes API, this operation is `POST /graphql` (base URL `https://app.launchnotes.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/archive-work-item.md) for the provider-specific parameters and requirements.

