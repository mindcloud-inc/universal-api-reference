# BSC Designer: Create Indicator Initiative



```
POST https://connect.mindcloud.co/v1/universal/bSCDesigner/latest/actions/create-indicator-initiative
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a BSC Designer `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/bSCDesigner/latest/actions/create-indicator-initiative" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "docId": "string",
  "guid": "string",
  "name": "Ava Chen",
  "status": "string",
  "initiativeType": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/bSCDesigner/latest/actions/create-indicator-initiative', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "docId": "string",
    "guid": "string",
    "name": "Ava Chen",
    "status": "string",
    "initiativeType": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `docId` | string | yes | Document id or alias containing the indicator. |
| `guid` | string | yes | Indicator guid for the new initiative. |
| `name` | string | yes | Initiative name. |
| `description` | string | no | Initiative description. |
| `status` | string | yes | Initiative status. |
| `showOnMap` | boolean | no | Whether the initiative should be shown on the map. |
| `initiativeType` | string | yes | Initiative type. |
| `budget` | number | no | Planned budget. |
| `currency` | string | no | Budget currency. |
| `duration` | number | no | Planned duration. |
| `durationUnit` | string | no | Duration unit. |
| `intervalStart` | string | no | Initiative start date. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "actualBudget": 1,
      "alignedInitiativesGuids": [
        "string"
      ],
      "alignedKpiGuid": "string",
      "author": "string",
      "budget": 1,
      "currency": "string",
      "description": "string",
      "documents": [
        {}
      ],
      "duration": 1,
      "durationUnit": "string",
      "guid": "string",
      "initiativeType": "string",
      "intervalEnd": "string",
      "intervalStart": "string",
      "name": "Ava Chen",
      "responsible": [
        "string"
      ],
      "showOnMap": true,
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `actualBudget` | number |  |
| `alignedInitiativesGuids` | array<string> |  |
| `alignedKpiGuid` | string |  |
| `author` | string |  |
| `budget` | number |  |
| `currency` | string |  |
| `description` | string |  |
| `documents` | array<object> |  |
| `duration` | number |  |
| `durationUnit` | string |  |
| `guid` | string |  |
| `initiativeType` | string |  |
| `intervalEnd` | string |  |
| `intervalStart` | string |  |
| `name` | string |  |
| `responsible` | array<string> |  |
| `showOnMap` | boolean |  |
| `status` | string |  |

## Native endpoint

Through the native BSC Designer API, this operation is `POST /rest/api/document/:docId/kpi/:guid/initiatives` (base URL `https://www.webbsc.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-indicator-initiative.md) for the provider-specific parameters and requirements.

