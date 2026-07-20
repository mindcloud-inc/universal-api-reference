# Clappia: Get App Workflow

Retrieves app workflow details from Clappia.

```
GET https://connect.mindcloud.co/v1/universal/clappia/latest/actions/get-app-workflow
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Clappia `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/clappia/latest/actions/get-app-workflow?connectionId=$CONNECTION_ID&appId=string&triggerType=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "appId": "string",
  "triggerType": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/clappia/latest/actions/get-app-workflow?${params}`, {
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
| `appId` | string | yes | Clappia app ID. |
| `triggerType` | string | yes | Workflow trigger type such as newSubmission, editSubmission, or reviewSubmission. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": 1,
      "lastUpdatedAt": 1,
      "lastUpdatedBy": {},
      "steps": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | number |  |
| `lastUpdatedAt` | number |  |
| `lastUpdatedBy` | object |  |
| `steps` | object |  |

## Native endpoint

Through the native Clappia API, this operation is `GET /workflowdefinitionv2/getWorkflow` (base URL `https://api-public-v4.clappia.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-app-workflow.md) for the provider-specific parameters and requirements.

