# Currents: List Failing Spec Files



```
GET https://connect.mindcloud.co/v1/universal/currents/latest/actions/list-failing-spec-files
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Currents `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/currents/latest/actions/list-failing-spec-files?connectionId=$CONNECTION_ID&dateEnd=string&dateStart=string&projectId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "dateEnd": "string",
  "dateStart": "string",
  "projectId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/currents/latest/actions/list-failing-spec-files?${params}`, {
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
| `dateEnd` | string | yes |  |
| `dateStart` | string | yes |  |
| `dir` | string | no |  |
| `projectId` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {
        "list": [
          {}
        ],
        "nextPage": true,
        "total": 1
      },
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data.list` | array<object> |  |
| `data.nextPage` | boolean |  |
| `data.total` | number |  |
| `status` | string |  |

## Native endpoint

Through the native Currents API, this operation is `GET /spec-files/:projectId` (base URL `https://api.currents.dev/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-failing-spec-files.md) for the provider-specific parameters and requirements.

