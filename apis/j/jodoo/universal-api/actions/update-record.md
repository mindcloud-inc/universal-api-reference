# Jodoo: Update Record



```
PUT https://connect.mindcloud.co/v1/universal/jodoo/latest/actions/update-record
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Jodoo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/jodoo/latest/actions/update-record" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "appId": "69c4042cce7f5503d03455c1",
  "entryId": "63e809d2b8c3070007093940",
  "dataId": "69c4042cce7f5503d034561b",
  "data": "[object Object]"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/jodoo/latest/actions/update-record', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "appId": "69c4042cce7f5503d03455c1",
    "entryId": "63e809d2b8c3070007093940",
    "dataId": "69c4042cce7f5503d034561b",
    "data": "[object Object]"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `appId` | string | yes | Jodoo app ID that owns the form. Example: `69c4042cce7f5503d03455c1`. |
| `entryId` | string | yes | Jodoo form ID that owns the record. Example: `63e809d2b8c3070007093940`. |
| `dataId` | string | yes | Jodoo record ID to update. Example: `69c4042cce7f5503d034561b`. |
| `data` | object | yes | Updated field payload keyed by Jodoo widget IDs. Each widget must be an object with a value property, for example {"_widget_x":{"value":"Updated Item"}}. Example: `[object Object]`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "appId": "string",
      "createTime": "2026-05-07T12:00:00.000Z",
      "creator": {
        "departments": [
          1
        ],
        "name": "Ava Chen",
        "status": 1,
        "type": 1,
        "username": "Ava Chen"
      },
      "entryId": "string",
      "id": "string",
      "updater": {
        "departments": [
          1
        ],
        "name": "Ava Chen",
        "status": 1,
        "type": 1,
        "username": "Ava Chen"
      },
      "updateTime": "2026-05-07T12:00:00.000Z",
      "widget1676151250976": "string",
      "widget1676151250977": "2026-05-07T12:00:00.000Z",
      "widget1676151250978": "string",
      "widget1676151250980": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `appId` | string |  |
| `createTime` | date |  |
| `creator.departments[]` | number |  |
| `creator.name` | string |  |
| `creator.status` | number |  |
| `creator.type` | number |  |
| `creator.username` | string |  |
| `entryId` | string |  |
| `id` | string |  |
| `updater.departments[]` | number |  |
| `updater.name` | string |  |
| `updater.status` | number |  |
| `updater.type` | number |  |
| `updater.username` | string |  |
| `updateTime` | date |  |
| `widget1676151250976` | string |  |
| `widget1676151250977` | date |  |
| `widget1676151250978` | string |  |
| `widget1676151250980` | number |  |

## Native endpoint

Through the native Jodoo API, this operation is `POST /app/entry/data/update` (base URL `https://api.jodoo.com/api/v5`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-record.md) for the provider-specific parameters and requirements.

