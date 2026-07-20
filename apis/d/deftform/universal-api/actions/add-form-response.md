# Deftform: Add Form Response

Creates a form response in Deftform.

```
POST https://connect.mindcloud.co/v1/universal/deftform/latest/actions/add-form-response
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Deftform `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/deftform/latest/actions/add-form-response" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "formId": "string",
  "data": "[object Object]"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/deftform/latest/actions/add-form-response', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "formId": "string",
    "data": "[object Object]"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `formId` | string | yes | The Deftform form ID that should receive the new response. |
| `data` | object | yes | Object mapping Deftform field UUIDs to string or integer response values. Example: `[object Object]`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "created_at": "2026-05-07T12:00:00.000Z",
      "uuid": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `created_at` | date | Response creation timestamp. |
| `uuid` | string | UUID of the submitted response. |

## Native endpoint

Through the native Deftform API, this operation is `POST /forms/:formId/response` (base URL `https://deftform.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-form-response.md) for the provider-specific parameters and requirements.

