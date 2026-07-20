# Ubiqod by Skiply: Add Badges To Badge List



```
PUT https://connect.mindcloud.co/v1/universal/ubiqodBySkiply/latest/actions/add-badges-to-badge-list
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Ubiqod by Skiply `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/ubiqodBySkiply/latest/actions/add-badges-to-badge-list" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "badgeListId": "string",
  "list[]": [
    {}
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/ubiqodBySkiply/latest/actions/add-badges-to-badge-list', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "badgeListId": "string",
    "list[]": [{}]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `badgeListId` | string | yes | Badge list ID. |
| `list[]` | array<object> | yes | Badges to add to the badge list. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "label": "string",
      "list": [
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
| `id` | string | Badge list ID. |
| `label` | string | Badge list label. |
| `list` | array<object> | Badges in the list. |

## Native endpoint

Through the native Ubiqod by Skiply API, this operation is `POST /badges/:badgeListId/codes` (base URL `https://api.ubiqod.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-badges-to-badge-list.md) for the provider-specific parameters and requirements.

