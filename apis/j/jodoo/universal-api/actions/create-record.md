# Jodoo: Create Record



```
POST https://connect.mindcloud.co/v1/universal/jodoo/latest/actions/create-record
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Jodoo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/jodoo/latest/actions/create-record" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "appId": "69c4042cce7f5503d03455c1",
  "entryId": "63e809d2b8c3070007093940",
  "data": "[object Object]"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/jodoo/latest/actions/create-record', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "appId": "69c4042cce7f5503d03455c1",
    "entryId": "63e809d2b8c3070007093940",
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
| `entryId` | string | yes | Jodoo form ID to create a record in. Example: `63e809d2b8c3070007093940`. |
| `data` | object | yes | Record field payload keyed by Jodoo widget IDs. Each widget must be an object with a value property, for example {"_widget_x":{"value":"Notebook"}}. Example: `[object Object]`. |

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
      "widget1676145679483": "string",
      "widget1676145679484": {
        "departments": [
          1
        ],
        "name": "Ava Chen",
        "status": 1,
        "type": 1,
        "username": "Ava Chen"
      },
      "widget1676145679485": [
        {
          "deptNo": 1,
          "name": "Ava Chen",
          "parentNo": 1,
          "status": 1,
          "type": 1
        }
      ],
      "widget1676146312982": "string",
      "widget1676146312984": "string"
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
| `widget1676145679483` | string |  |
| `widget1676145679484.departments[]` | number |  |
| `widget1676145679484.name` | string |  |
| `widget1676145679484.status` | number |  |
| `widget1676145679484.type` | number |  |
| `widget1676145679484.username` | string |  |
| `widget1676145679485[].deptNo` | number |  |
| `widget1676145679485[].name` | string |  |
| `widget1676145679485[].parentNo` | number |  |
| `widget1676145679485[].status` | number |  |
| `widget1676145679485[].type` | number |  |
| `widget1676146312982` | string |  |
| `widget1676146312984` | string |  |

## Native endpoint

Through the native Jodoo API, this operation is `POST /app/entry/data/create` (base URL `https://api.jodoo.com/api/v5`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-record.md) for the provider-specific parameters and requirements.

