# Showcase Workshop: Add Data

Creates a data item in Showcase Workshop.

```
POST https://connect.mindcloud.co/v1/universal/showcaseWorkshop/latest/actions/add-data
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Showcase Workshop `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/showcaseWorkshop/latest/actions/add-data" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "dataName": "Form1",
  "showcaseId": 1,
  "userEmail": "name@example.com",
  "content": "[object Object]",
  "dateEntered": "2013-01-28T13:01:01Z"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/showcaseWorkshop/latest/actions/add-data', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "dataName": "Form1",
    "showcaseId": 1,
    "userEmail": "name@example.com",
    "content": "[object Object]",
    "dateEntered": "2013-01-28T13:01:01Z"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `dataName` | string | yes | Name for the submitted data payload. Example: `Form1`. |
| `showcaseId` | number | yes | Numeric Showcase identifier that the data belongs to. |
| `userEmail` | string | yes | Email address associated with the data submission. Example: `name@example.com`. |
| `content` | string | yes | Submitted content as a JSON string. Example: `[object Object]`. |
| `dateEntered` | date | yes | ISO 8601 timestamp when the data was entered. Example: `2013-01-28T13:01:01Z`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "content": "string",
      "dataName": "Ava Chen",
      "dataType": "string",
      "dateInserted": "2026-05-07T12:00:00.000Z",
      "guid": "string",
      "showcaseId": 1,
      "showcaseName": "Ava Chen",
      "userEmail": "ava@example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `content` | string |  |
| `dataName` | string |  |
| `dataType` | string |  |
| `dateInserted` | date |  |
| `guid` | string |  |
| `showcaseId` | number |  |
| `showcaseName` | string |  |
| `userEmail` | string |  |

## Native endpoint

Through the native Showcase Workshop API, this operation is `POST /data/` (base URL `https://app.showcaseworkshop.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-data.md) for the provider-specific parameters and requirements.

