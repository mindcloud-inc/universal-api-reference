# Kintone: Add Record

Creates a record in Kintone.

```
POST https://connect.mindcloud.co/v1/universal/kintone/latest/actions/add-record
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Kintone `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/kintone/latest/actions/add-record" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "appId": 1,
  "record": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/kintone/latest/actions/add-record', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "appId": 1,
    "record": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `appId` | number | yes | The Kintone app ID. |
| `record` | object | yes | The record payload keyed by Kintone field code. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "revision": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string | The created record ID. |
| `revision` | string | The new revision number for the created record. |

## Native endpoint

Through the native Kintone API, this operation is `POST /record.json` (base URL `{{credentials.baseUrl}}/k/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-record.md) for the provider-specific parameters and requirements.

