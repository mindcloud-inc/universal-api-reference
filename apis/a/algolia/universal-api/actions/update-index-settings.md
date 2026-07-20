# Algolia: Update Index Settings

Updates existing index settings in Algolia.

```
PUT https://connect.mindcloud.co/v1/universal/algolia/latest/actions/update-index-settings
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Algolia `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/algolia/latest/actions/update-index-settings" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "indexName": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/algolia/latest/actions/update-index-settings', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "indexName": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `indexName` | string | yes | The name of the Algolia index. |
| `attributesForFaceting[]` | array<string> | no | Facet configuration entries for the index. |
| `hitsPerPage` | number | no | Default number of hits per page. |
| `paginationLimitedTo` | number | no | Maximum number of hits available through pagination. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `forwardToReplicas` | boolean | no | Whether to apply the same settings to replica indices. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "taskID": 1,
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `taskID` | number |  |
| `updatedAt` | date |  |

## Native endpoint

Through the native Algolia API, this operation is `PUT /1/indexes/:indexName/settings` (base URL `https://{{credentials.applicationId}}.algolia.net`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-index-settings.md) for the provider-specific parameters and requirements.

