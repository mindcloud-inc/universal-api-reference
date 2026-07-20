# BSC Designer: Get Indicator Initiative



```
GET https://connect.mindcloud.co/v1/universal/bSCDesigner/latest/actions/get-indicator-initiative
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a BSC Designer `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bSCDesigner/latest/actions/get-indicator-initiative?connectionId=$CONNECTION_ID&docId=string&guid=string&initiativeGuid=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "docId": "string",
  "guid": "string",
  "initiativeGuid": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/bSCDesigner/latest/actions/get-indicator-initiative?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `docId` | string | yes | Document id or alias containing the indicator. |
| `guid` | string | yes | Indicator guid containing the initiative. |
| `initiativeGuid` | string | yes | Initiative guid to retrieve. |

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

Through the native BSC Designer API, this operation is `GET /rest/api/document/:docId/kpi/:guid/initiatives/:initiativeGuid` (base URL `https://www.webbsc.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-indicator-initiative.md) for the provider-specific parameters and requirements.

