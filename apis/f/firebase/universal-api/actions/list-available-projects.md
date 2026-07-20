# Firebase: List Available Projects

Retrieves available Google Cloud projects for Firebase.

```
GET https://connect.mindcloud.co/v1/universal/firebase/latest/actions/list-available-projects
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Firebase `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/firebase/latest/actions/list-available-projects?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/firebase/latest/actions/list-available-projects?${params}`, {
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
      "displayName": "Ava Chen",
      "locationId": "string",
      "project": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `displayName` | string | Display name of the Google Cloud project. |
| `locationId` | string | Default resource location ID, when available. |
| `project` | string | Resource name of the Google Cloud project. |

## Native endpoint

Through the native Firebase API, this operation is `GET /v1beta1/availableProjects` (base URL `https://firebase.googleapis.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-available-projects.md) for the provider-specific parameters and requirements.

