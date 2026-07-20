# Currents: List Failing Tests



```
GET https://connect.mindcloud.co/v1/universal/currents/latest/actions/list-failing-tests
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Currents `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/currents/latest/actions/list-failing-tests?connectionId=$CONNECTION_ID&dateEnd=string&dateStart=string&projectId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "dateEnd": "string",
  "dateStart": "string",
  "projectId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/currents/latest/actions/list-failing-tests?${params}`, {
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
| `projectId` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {
        "count": 1,
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
| `data.count` | number |  |
| `data.list` | array<object> |  |
| `data.nextPage` | boolean |  |
| `data.total` | number |  |
| `status` | string |  |

## Native endpoint

Through the native Currents API, this operation is `GET /tests/:projectId` (base URL `https://api.currents.dev/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-failing-tests.md) for the provider-specific parameters and requirements.

