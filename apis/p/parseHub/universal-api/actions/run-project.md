# ParseHub: Run Project



```
POST https://connect.mindcloud.co/v1/universal/parseHub/latest/actions/run-project
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ParseHub `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/parseHub/latest/actions/run-project" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "projectToken": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/parseHub/latest/actions/run-project', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "projectToken": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `projectToken` | string | yes | The ParseHub token of the project to run. |
| `startUrl` | string | no | Optional URL to override the project's default start site. |
| `startTemplate` | string | no | Optional template name to start the run with. |
| `sendEmail` | number | no | Set to 1 to send an email when the run completes or errors. Default: `0`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `startValueOverride` | string | no | Optional JSON string of starting global-scope values for the run, such as {"query":"San Francisco"}. |

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

Through the native ParseHub API, this operation is `POST /projects/{project_token}/run` (base URL `https://www.parsehub.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/run-project.md) for the provider-specific parameters and requirements.

