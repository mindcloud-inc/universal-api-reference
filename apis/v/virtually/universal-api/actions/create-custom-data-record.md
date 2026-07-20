# Virtually: Create Custom Data Record

Creates a new custom data record in Virtually.

```
POST https://connect.mindcloud.co/v1/universal/virtually/latest/actions/create-custom-data-record
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Virtually `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/virtually/latest/actions/create-custom-data-record" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "data[]": [
    {}
  ],
  "data[].memberId": "string",
  "data[].properties": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/virtually/latest/actions/create-custom-data-record', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "data[]": [{}],
    "data[].memberId": "string",
    "data[].properties": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `data[]` | array<object> | yes | The custom data records to create. |
| `data[].memberId` | string | yes | The member ID. |
| `data[].ts` | number | no | Optional event timestamp. |
| `data[].event` | string | no | Optional event name. |
| `data[].properties` | object | yes | Custom properties. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "logsIngested": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `logsIngested` | number |  |

## Native endpoint

Through the native Virtually API, this operation is `POST /api/v2/orgs/:orgId/customData` (base URL `https://app.tryvirtually.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-custom-data-record.md) for the provider-specific parameters and requirements.

