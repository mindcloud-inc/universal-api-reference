# Kite Suite: Reset default custom Field by project Id



```
PUT https://connect.mindcloud.co/v1/universal/kiteSuiteCustom/latest/actions/reset-default-custom-field-by-project-id
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Kite Suite `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/kiteSuiteCustom/latest/actions/reset-default-custom-field-by-project-id" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/kiteSuiteCustom/latest/actions/reset-default-custom-field-by-project-id', {
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
| `id` | string | yes | project ID |

## Response

```json
{
  "success": true,
  "data": [
    {
      "_id": "string",
      "currencyType": "string",
      "description": "string",
      "fieldOptions": [
        "string"
      ],
      "fieldTitle": "string",
      "fieldType": "string",
      "isEnable": true,
      "isPredefined": true,
      "isRestricted": true,
      "isTrashed": true,
      "predefinedId": "string",
      "projectID": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `_id` | string | ID of the custom field |
| `currencyType` | string | Currency type of custom field |
| `description` | string |  |
| `fieldOptions` | array |  |
| `fieldTitle` | string | Field title |
| `fieldType` | string | Type of custom field |
| `isEnable` | boolean |  |
| `isPredefined` | boolean |  |
| `isRestricted` | boolean | restricted status of custom field |
| `isTrashed` | boolean | trash status of custom field |
| `predefinedId` | string |  |
| `projectID` | string | project ID of project |

## Native endpoint

Through the native Kite Suite API, this operation is `PATCH /api/v1/custom-field/project/:id` (base URL `https://api.kitesuite.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/reset-default-custom-field-by-project-id.md) for the provider-specific parameters and requirements.

