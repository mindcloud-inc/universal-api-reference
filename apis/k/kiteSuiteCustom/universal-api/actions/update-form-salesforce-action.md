# Kite Suite: Update Form Salesforce Action



```
PUT https://connect.mindcloud.co/v1/universal/kiteSuiteCustom/latest/actions/update-form-salesforce-action
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Kite Suite `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/kiteSuiteCustom/latest/actions/update-form-salesforce-action" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "body": {},
  "id": "string",
  "objectKey": "string",
  "actionType": "string",
  "upsert": true,
  "createData[]": [
    "string"
  ],
  "matchData[]": [
    "string"
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/kiteSuiteCustom/latest/actions/update-form-salesforce-action', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "body": {},
    "id": "string",
    "objectKey": "string",
    "actionType": "string",
    "upsert": true,
    "createData[]": ["string"],
    "matchData[]": ["string"]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `body` | object | yes | Request body |
| `id` | string | yes | ID of the Salesforce action to update. |
| `objectKey` | string | yes | Updated key of the Salesforce object. |
| `actionType` | string | yes | Updated type of Salesforce action. |
| `upsert` | boolean | yes | Updated flag for upsert action. |
| `createData[]` | array | yes | Updated array of Salesforce fields and corresponding form fields for create/update. |
| `matchData[]` | array | yes | Updated array of Salesforce fields and corresponding form fields for matching in upsert. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "value": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `value` | object | Updated form integration object. |

## Native endpoint

Through the native Kite Suite API, this operation is `PATCH /api/v1/form/integration/salesforce/actions/:id` (base URL `https://api.kitesuite.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-form-salesforce-action.md) for the provider-specific parameters and requirements.

