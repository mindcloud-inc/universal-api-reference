# Kite Suite: Create Form Salesforce Action



```
POST https://connect.mindcloud.co/v1/universal/kiteSuiteCustom/latest/actions/create-form-salesforce-action
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Kite Suite `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/kiteSuiteCustom/latest/actions/create-form-salesforce-action" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "body": {},
  "form": "string",
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
const response = await fetch('https://connect.mindcloud.co/v1/universal/kiteSuiteCustom/latest/actions/create-form-salesforce-action', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "body": {},
    "form": "string",
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
| `form` | string | yes | ID of the form. |
| `objectKey` | string | yes | Key of the Salesforce object. |
| `actionType` | string | yes | Type of Salesforce action. |
| `upsert` | boolean | yes | Flag for upsert action. |
| `createData[]` | array | yes | Array of Salesforce fields and corresponding form fields for create/update. |
| `matchData[]` | array | yes | Array of Salesforce fields and corresponding form fields for matching in upsert. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Kite Suite API returns.

## Native endpoint

Through the native Kite Suite API, this operation is `POST /api/v1/form/integration/salesforce/actions` (base URL `https://api.kitesuite.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-form-salesforce-action.md) for the provider-specific parameters and requirements.

