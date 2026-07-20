# Kite Suite: Sync directory



```
POST https://connect.mindcloud.co/v1/universal/kiteSuiteCustom/latest/actions/sync-directory
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Kite Suite `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/kiteSuiteCustom/latest/actions/sync-directory" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "body": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/kiteSuiteCustom/latest/actions/sync-directory', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "body": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `body` | object | yes | Request body |

## Response

```json
{
  "success": true,
  "data": [
    {
      "_id": "string",
      "domains": [
        "string"
      ],
      "isEnable": true,
      "isTrashed": true,
      "name": "Ava Chen",
      "owner": "string",
      "syncActivity": [
        "string"
      ],
      "token": "string",
      "type": "string",
      "workspace": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `_id` | string | ID of the Directory |
| `domains` | array |  |
| `isEnable` | boolean | sync status of this directory |
| `isTrashed` | boolean | trash status of this directory* |
| `name` | string | name of directory |
| `owner` | string | owner of the this Directory |
| `syncActivity` | array |  |
| `token` | string |  |
| `type` | string |  |
| `workspace` | string | org ID of directory |

## Native endpoint

Through the native Kite Suite API, this operation is `POST /api/v1/directory/sync` (base URL `https://api.kitesuite.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/sync-directory.md) for the provider-specific parameters and requirements.

