# ParseHub: Get Project



```
GET https://connect.mindcloud.co/v1/universal/parseHub/latest/actions/get-project
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ParseHub `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/parseHub/latest/actions/get-project?connectionId=$CONNECTION_ID&projectToken=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "projectToken": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/parseHub/latest/actions/get-project?${params}`, {
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
| `projectToken` | string | yes | The ParseHub token of the project to fetch. |
| `offset` | number | no | Zero-based offset into the project's run_list. Default: `0`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `includeOptions` | number | no | Set to 1 to include project options_json in the response. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "lastReadyRun": {
        "runToken": "string"
      },
      "lastRun": {
        "runToken": "string"
      },
      "mainSite": "string",
      "mainTemplate": "string",
      "optionsJson": "string",
      "runList": [
        {
          "dataReady": true,
          "runToken": "string",
          "status": "string"
        }
      ],
      "templatesJson": "string",
      "title": "string",
      "token": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `lastReadyRun.runToken` | string |  |
| `lastRun.runToken` | string |  |
| `mainSite` | string |  |
| `mainTemplate` | string |  |
| `optionsJson` | string |  |
| `runList` | array<object> |  |
| `runList[].dataReady` | boolean |  |
| `runList[].runToken` | string |  |
| `runList[].status` | string |  |
| `templatesJson` | string |  |
| `title` | string |  |
| `token` | string |  |

## Native endpoint

Through the native ParseHub API, this operation is `GET /projects/{project_token}` (base URL `https://www.parsehub.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-project.md) for the provider-specific parameters and requirements.

