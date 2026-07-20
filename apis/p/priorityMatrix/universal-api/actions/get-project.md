# Priority Matrix: Get Project

Retrieves a project from Priority Matrix by IDD.

```
GET https://connect.mindcloud.co/v1/universal/priorityMatrix/latest/actions/get-project
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Priority Matrix `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/priorityMatrix/latest/actions/get-project?connectionId=$CONNECTION_ID&idd=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "idd": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/priorityMatrix/latest/actions/get-project?${params}`, {
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
| `idd` | number | yes | Project IDD. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "creationDate": 1,
      "idd": 1,
      "name": "Ava Chen",
      "resource_uri": "string",
      "state": 1,
      "webLink": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `creationDate` | number |  |
| `idd` | number |  |
| `name` | string |  |
| `resource_uri` | string |  |
| `state` | number |  |
| `webLink` | string |  |

## Native endpoint

Through the native Priority Matrix API, this operation is `GET /api/v1/project/:idd/` (base URL `https://sync.appfluence.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-project.md) for the provider-specific parameters and requirements.

