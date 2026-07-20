# Sleekplan: Edit Update



```
PUT https://connect.mindcloud.co/v1/universal/sleekplan/latest/actions/edit-update
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Sleekplan `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/sleekplan/latest/actions/edit-update" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "updateId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/sleekplan/latest/actions/edit-update', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "updateId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `updateId` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "changelogId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `changelogId` | string |  |

## Native endpoint

Through the native Sleekplan API, this operation is `PUT /update/:updateid` (base URL `https://api.sleekplan.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/edit-update.md) for the provider-specific parameters and requirements.

