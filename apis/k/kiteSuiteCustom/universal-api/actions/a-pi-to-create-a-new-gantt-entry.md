# Kite Suite: API to create a new Gantt entry



```
POST https://connect.mindcloud.co/v1/universal/kiteSuiteCustom/latest/actions/a-pi-to-create-a-new-gantt-entry
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Kite Suite `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/kiteSuiteCustom/latest/actions/a-pi-to-create-a-new-gantt-entry" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "body": {},
  "title": "string",
  "projectID": "string",
  "createdBy": "string",
  "isEnable": true,
  "view": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/kiteSuiteCustom/latest/actions/a-pi-to-create-a-new-gantt-entry', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "body": {},
    "title": "string",
    "projectID": "string",
    "createdBy": "string",
    "isEnable": true,
    "view": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `body` | object | yes | Request body |
| `title` | string | yes |  |
| `projectID` | string | yes |  |
| `createdBy` | string | yes |  |
| `isEnable` | boolean | yes |  |
| `view` | string | yes |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Kite Suite API returns.

## Native endpoint

Through the native Kite Suite API, this operation is `POST /api/v1/gantt` (base URL `https://api.kitesuite.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/a-pi-to-create-a-new-gantt-entry.md) for the provider-specific parameters and requirements.

