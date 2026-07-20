# ActiveCollab: List Project Labels

Retrieves project labels from your ActiveCollab workspace.

```
GET https://connect.mindcloud.co/v1/universal/activeCollab/latest/actions/list-project-labels
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ActiveCollab `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/activeCollab/latest/actions/list-project-labels?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/activeCollab/latest/actions/list-project-labels?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "class": "string",
      "color": "string",
      "darkerTextColor": "string",
      "id": 1,
      "isDefault": true,
      "lighterTextColor": "string",
      "name": "Ava Chen",
      "position": 1,
      "projectId": {},
      "updatedOn": {},
      "urlPath": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `class` | string |  |
| `color` | string |  |
| `darkerTextColor` | string |  |
| `id` | number |  |
| `isDefault` | boolean |  |
| `lighterTextColor` | string |  |
| `name` | string |  |
| `position` | number |  |
| `projectId` | object |  |
| `updatedOn` | object |  |
| `urlPath` | string |  |

## Native endpoint

Through the native ActiveCollab API, this operation is `GET /labels/project-labels` (base URL `https://app.activecollab.com/:instanceId/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-project-labels.md) for the provider-specific parameters and requirements.

