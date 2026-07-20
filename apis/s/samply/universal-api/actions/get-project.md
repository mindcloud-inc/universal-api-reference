# Samply: Get Project



```
GET https://connect.mindcloud.co/v1/universal/samply/latest/actions/get-project
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Samply `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/samply/latest/actions/get-project?connectionId=$CONNECTION_ID&projectid=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "projectid": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/samply/latest/actions/get-project?${params}`, {
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
| `projectid` | string | yes | The Samply project id. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "artwork": "string",
      "color": "string",
      "creator": {},
      "id": "string",
      "name": "Ava Chen",
      "object": "string",
      "size": 1,
      "sortBy": {},
      "timeCreated": 1,
      "timeModified": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `artwork` | string |  |
| `color` | string |  |
| `creator` | object |  |
| `id` | string |  |
| `name` | string |  |
| `object` | string |  |
| `size` | number |  |
| `sortBy` | object |  |
| `timeCreated` | number |  |
| `timeModified` | number |  |

## Native endpoint

Through the native Samply API, this operation is `GET /projects/:projectid` (base URL `https://samply.app/api/v0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-project.md) for the provider-specific parameters and requirements.

