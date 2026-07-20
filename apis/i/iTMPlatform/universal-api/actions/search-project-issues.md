# ITM Platform: Search Project Issues



```
GET https://connect.mindcloud.co/v1/universal/iTMPlatform/latest/actions/search-project-issues
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ITM Platform `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/iTMPlatform/latest/actions/search-project-issues?connectionId=$CONNECTION_ID&projectId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "projectId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/iTMPlatform/latest/actions/search-project-issues?${params}`, {
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
      "changeInProjectCost": {},
      "changeInProjectScheduleDays": 1,
      "description": "string",
      "id": 1,
      "managementCost": {},
      "managementHours": "string",
      "name": "Ava Chen",
      "type": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `changeInProjectCost` | object |  |
| `changeInProjectScheduleDays` | number |  |
| `description` | string |  |
| `id` | number |  |
| `managementCost` | object |  |
| `managementHours` | string |  |
| `name` | string |  |
| `type` | object |  |

## Native endpoint

Through the native ITM Platform API, this operation is `GET /v2/Projects/{ProjectId}/Issues/Search` (base URL `https://api.itmplatform.com/{{credentials.company}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-project-issues.md) for the provider-specific parameters and requirements.

