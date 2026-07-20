# Castor EDC: Request Multi Export

Requests multiple study exports in Castor EDC.

```
POST https://connect.mindcloud.co/v1/universal/castorEDC/latest/actions/request-multi-export
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Castor EDC `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/castorEDC/latest/actions/request-multi-export" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "study_id": "string",
  "exports": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/castorEDC/latest/actions/request-multi-export', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "study_id": "string",
    "exports": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `study_id` | string | yes | The ID of the study for which this call should be made |
| `exports` | object | yes | Batch export request definition |

## Response

```json
{
  "success": true,
  "data": [
    {
      "description": "string",
      "queued_exports": [
        "string"
      ],
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `description` | string |  |
| `queued_exports[]` | string |  |
| `success` | boolean |  |

## Native endpoint

Through the native Castor EDC API, this operation is `POST /study/:study_id/export` (base URL `https://us.castoredc.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/request-multi-export.md) for the provider-specific parameters and requirements.

