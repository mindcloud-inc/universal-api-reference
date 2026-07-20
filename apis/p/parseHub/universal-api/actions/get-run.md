# ParseHub: Get Run



```
GET https://connect.mindcloud.co/v1/universal/parseHub/latest/actions/get-run
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ParseHub `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/parseHub/latest/actions/get-run?connectionId=$CONNECTION_ID&runToken=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "runToken": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/parseHub/latest/actions/get-run?${params}`, {
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
| `runToken` | string | yes | The ParseHub token of the run to fetch. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "dataReady": true,
      "endTime": "string",
      "md5sum": "string",
      "pages": 1,
      "projectToken": "string",
      "runToken": "string",
      "startTemplate": "string",
      "startTime": "string",
      "startUrl": "https://example.com",
      "startValue": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `dataReady` | boolean |  |
| `endTime` | string |  |
| `md5sum` | string |  |
| `pages` | number |  |
| `projectToken` | string |  |
| `runToken` | string |  |
| `startTemplate` | string |  |
| `startTime` | string |  |
| `startUrl` | string |  |
| `startValue` | string |  |
| `status` | string |  |

## Native endpoint

Through the native ParseHub API, this operation is `GET /runs/{run_token}` (base URL `https://www.parsehub.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-run.md) for the provider-specific parameters and requirements.

