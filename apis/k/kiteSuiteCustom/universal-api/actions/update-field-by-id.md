# Kite Suite: Update Field by Id



```
PUT https://connect.mindcloud.co/v1/universal/kiteSuiteCustom/latest/actions/update-field-by-id
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Kite Suite `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/kiteSuiteCustom/latest/actions/update-field-by-id" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/kiteSuiteCustom/latest/actions/update-field-by-id', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes | Update field ID |

## Response

```json
{
  "success": true,
  "data": [
    {
      "_id": "string",
      "isChecked": true,
      "isTrashed": true,
      "task": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `_id` | string | ID of the field |
| `isChecked` | boolean |  |
| `isTrashed` | boolean | trash status of field |
| `task` | string | task id |

## Native endpoint

Through the native Kite Suite API, this operation is `PATCH /api/v1/check-list/:id` (base URL `https://api.kitesuite.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-field-by-id.md) for the provider-specific parameters and requirements.

