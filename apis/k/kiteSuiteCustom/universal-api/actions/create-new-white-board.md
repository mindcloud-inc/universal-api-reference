# Kite Suite: Create new White Board



```
POST https://connect.mindcloud.co/v1/universal/kiteSuiteCustom/latest/actions/create-new-white-board
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Kite Suite `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/kiteSuiteCustom/latest/actions/create-new-white-board" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "body": {},
  "name": "Ava Chen",
  "projectID": "string",
  "json": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/kiteSuiteCustom/latest/actions/create-new-white-board', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "body": {},
    "name": "Ava Chen",
    "projectID": "string",
    "json": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `body` | object | yes | Request body |
| `name` | string | yes |  |
| `projectID` | string | yes |  |
| `json` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "_id": "string",
      "createdBy": "string",
      "isTrashed": true,
      "json": "string",
      "name": "Ava Chen",
      "projectID": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `_id` | string | ID of the WhiteBoard |
| `createdBy` | string | creator of the this WhiteBoard |
| `isTrashed` | boolean | trash status of this WhiteBoard |
| `json` | string |  |
| `name` | string | name of WhiteBoard |
| `projectID` | string | project ID of WhiteBoard |

## Native endpoint

Through the native Kite Suite API, this operation is `POST /api/v1/white-board` (base URL `https://api.kitesuite.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-new-white-board.md) for the provider-specific parameters and requirements.

