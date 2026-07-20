# Florm: Export Form Analytics

Creates an export task for Florm form analytics.

```
POST https://connect.mindcloud.co/v1/universal/florm/latest/actions/export-form-analytics
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Florm `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/florm/latest/actions/export-form-analytics" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "type": "string",
  "formGuid": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/florm/latest/actions/export-form-analytics', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "type": "string",
    "formGuid": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `type` | string | yes | Export file type. |
| `formGuid` | string | yes | GUID of the Florm form to export analytics for. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "resultString": "string",
      "status": "string",
      "taskGuid": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `resultString` | string | Provider result string when available. |
| `status` | string | Current export task status. |
| `taskGuid` | string | GUID of the created export task. |

## Native endpoint

Through the native Florm API, this operation is `POST /v1/export/form/analytics` (base URL `https://api.florm.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/export-form-analytics.md) for the provider-specific parameters and requirements.

