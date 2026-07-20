# Jodoo: Get Record



```
GET https://connect.mindcloud.co/v1/universal/jodoo/latest/actions/get-record
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Jodoo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/jodoo/latest/actions/get-record?connectionId=$CONNECTION_ID&appId=69c4042cce7f5503d03455c1&entryId=63e809d2b8c3070007093940&dataId=680fd754bfb1d100090f5c10" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "appId": "69c4042cce7f5503d03455c1",
  "entryId": "63e809d2b8c3070007093940",
  "dataId": "680fd754bfb1d100090f5c10"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/jodoo/latest/actions/get-record?${params}`, {
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
| `appId` | string | yes | Jodoo app ID that owns the form. Example: `69c4042cce7f5503d03455c1`. |
| `entryId` | string | yes | Jodoo form ID. Example: `63e809d2b8c3070007093940`. |
| `dataId` | string | yes | Jodoo record ID to fetch. Example: `680fd754bfb1d100090f5c10`. |

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

Through the native Jodoo API, this operation is `POST /app/entry/data/get` (base URL `https://api.jodoo.com/api/v5`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-record.md) for the provider-specific parameters and requirements.

