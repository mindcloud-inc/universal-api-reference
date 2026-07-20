# ITM Platform: Search Project Sprints



```
GET https://connect.mindcloud.co/v1/universal/iTMPlatform/latest/actions/search-project-sprints
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ITM Platform `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/iTMPlatform/latest/actions/search-project-sprints?connectionId=$CONNECTION_ID&projectId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "projectId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/iTMPlatform/latest/actions/search-project-sprints?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `projectId` | string | yes | The ITM Platform project ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "accountId": 1,
      "description": "string",
      "duration": "string",
      "id": "string",
      "languageId": 1,
      "name": "Ava Chen",
      "projectId": 1,
      "startDate": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accountId` | number |  |
| `description` | string |  |
| `duration` | string |  |
| `id` | string |  |
| `languageId` | number |  |
| `name` | string |  |
| `projectId` | number |  |
| `startDate` | string |  |

## Native endpoint

Through the native ITM Platform API, this operation is `POST /v2/Projects/{ProjectId}/Sprints/Search` (base URL `https://api.itmplatform.com/{{credentials.company}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-project-sprints.md) for the provider-specific parameters and requirements.

