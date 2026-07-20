# Kintone: Update Status

Updates a record status in Kintone.

```
PUT https://connect.mindcloud.co/v1/universal/kintone/latest/actions/update-status
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Kintone `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/kintone/latest/actions/update-status" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "appId": 1,
  "recordId": 1,
  "actionName": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/kintone/latest/actions/update-status', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "appId": 1,
    "recordId": 1,
    "actionName": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `appId` | number | yes | The Kintone app ID. |
| `recordId` | number | yes | The Kintone record ID. |
| `actionName` | string | yes | The process management action name to apply. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `assignee` | string | no | Optional user code to assign during the status transition. |
| `revision` | number | no | The expected record revision number. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "revision": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `revision` | string | The new revision number after the status update succeeds. |

## Native endpoint

Through the native Kintone API, this operation is `PUT /record/status.json` (base URL `{{credentials.baseUrl}}/k/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-status.md) for the provider-specific parameters and requirements.

