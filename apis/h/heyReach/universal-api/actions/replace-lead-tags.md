# Hey Reach: Replace Lead Tags

Replaces tags for a lead in Hey Reach.

```
PUT https://connect.mindcloud.co/v1/universal/heyReach/latest/actions/replace-lead-tags
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Hey Reach `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/heyReach/latest/actions/replace-lead-tags" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "tags[]": [
    "string"
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/heyReach/latest/actions/replace-lead-tags', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "tags[]": ["string"]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `leadProfileUrl` | string | no |  |
| `leadLinkedInId` | string | no |  |
| `tags[]` | array<string> | yes |  |
| `createTagIfNotExisting` | boolean | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "newAssignedTags": [
        "string"
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `newAssignedTags` | array<string> |  |

## Native endpoint

Through the native Hey Reach API, this operation is `POST /api/public/lead/ReplaceTags` (base URL `https://api.heyreach.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/replace-lead-tags.md) for the provider-specific parameters and requirements.

