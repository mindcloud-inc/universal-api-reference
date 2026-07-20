# Productlane: Move Articles To Group

Moves help center articles to a Productlane doc group.

```
PUT https://connect.mindcloud.co/v1/universal/productlane/latest/actions/move-articles-to-group
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Productlane `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/productlane/latest/actions/move-articles-to-group" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "articleIds[]": "95697bff-03d3-4ca1-b079-a153436116ba",
  "groupId": "a48ae618-61e4-4ec1-b23a-56ac476c95d5"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/productlane/latest/actions/move-articles-to-group', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "articleIds[]": "95697bff-03d3-4ca1-b079-a153436116ba",
    "groupId": "a48ae618-61e4-4ec1-b23a-56ac476c95d5"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `articleIds[]` | array<string> | yes | One or more doc article IDs to move. Example: `95697bff-03d3-4ca1-b079-a153436116ba`. |
| `groupId` | string | yes | Target docs group ID, or null to ungroup. Example: `a48ae618-61e4-4ec1-b23a-56ac476c95d5`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "updatedCount": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `updatedCount` | number |  |

## Native endpoint

Through the native Productlane API, this operation is `POST /docs/groups/move-articles` (base URL `https://productlane.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/move-articles-to-group.md) for the provider-specific parameters and requirements.

