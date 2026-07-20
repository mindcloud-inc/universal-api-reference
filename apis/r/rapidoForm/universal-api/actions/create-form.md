# RapidoForm: Create Form

Creates a new form in RapidoForm.

```
POST https://connect.mindcloud.co/v1/universal/rapidoForm/latest/actions/create-form
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a RapidoForm `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/rapidoForm/latest/actions/create-form" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "surveyName": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/rapidoForm/latest/actions/create-form', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "surveyName": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `surveyName` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "2026-05-07T12:00:00.000Z",
      "creatorId": "string",
      "Id": 1,
      "isVpnIntegrationAdded": true,
      "randamizationCondition": true,
      "status": "string",
      "surveyName": "Ava Chen",
      "themeId": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "V": 1,
      "workspaceId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | date |  |
| `creatorId` | string |  |
| `Id` | number |  |
| `isVpnIntegrationAdded` | boolean |  |
| `randamizationCondition` | boolean |  |
| `status` | string |  |
| `surveyName` | string |  |
| `themeId` | string |  |
| `updatedAt` | date |  |
| `V` | number |  |
| `workspaceId` | string |  |

## Native endpoint

Through the native RapidoForm API, this operation is `POST /api/survey/create` (base URL `https://www.rapidoform.com/be`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-form.md) for the provider-specific parameters and requirements.

