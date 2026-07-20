# SIGNL4: Get Alert Timeline

Retrieves an alert timeline from SIGNL4.

```
GET https://connect.mindcloud.co/v1/universal/sIGNL4/latest/actions/get-alert-timeline
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SIGNL4 `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sIGNL4/latest/actions/get-alert-timeline?connectionId=$CONNECTION_ID&alertId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "alertId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sIGNL4/latest/actions/get-alert-timeline?${params}`, {
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
| `alertId` | string | yes | Id of the requested Alert. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `userId` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "annotationtype": 1,
      "creatorId": "string",
      "creatorType": 1,
      "entrytype": 1,
      "id": "string",
      "order": 1,
      "remoteActionId": "string",
      "remoteJobId": "string",
      "teamId": "string",
      "text": "string",
      "timestamp": "2026-05-07T12:00:00.000Z",
      "userId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `annotationtype` | number |  |
| `creatorId` | string |  |
| `creatorType` | number |  |
| `entrytype` | number |  |
| `id` | string |  |
| `order` | number |  |
| `remoteActionId` | string |  |
| `remoteJobId` | string |  |
| `teamId` | string |  |
| `text` | string |  |
| `timestamp` | date |  |
| `userId` | string |  |

## Native endpoint

Through the native SIGNL4 API, this operation is `GET /v2/alerts/{alertId}/timeline` (base URL `https://connect.signl4.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-alert-timeline.md) for the provider-specific parameters and requirements.

