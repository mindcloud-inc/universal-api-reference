# Superthread: Update Page Property



```
PUT https://connect.mindcloud.co/v1/universal/superthread/latest/actions/update-page-property
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Superthread `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/superthread/latest/actions/update-page-property" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "teamId": "string",
  "pageId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/superthread/latest/actions/update-page-property', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "teamId": "string",
    "pageId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `teamId` | string | yes | Workspace ID for the Superthread workspace. |
| `title` | string | no | Page title. |
| `pageId` | string | yes | Page ID to update. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "page": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `page` | object |  |

## Native endpoint

Through the native Superthread API, this operation is `PATCH /:team_id/pages/:page_id` (base URL `https://api.superthread.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-page-property.md) for the provider-specific parameters and requirements.

