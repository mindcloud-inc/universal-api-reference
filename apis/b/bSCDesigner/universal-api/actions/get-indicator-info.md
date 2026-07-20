# BSC Designer: Get Indicator Info



```
GET https://connect.mindcloud.co/v1/universal/bSCDesigner/latest/actions/get-indicator-info
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a BSC Designer `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bSCDesigner/latest/actions/get-indicator-info?connectionId=$CONNECTION_ID&docId=string&guid=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "docId": "string",
  "guid": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/bSCDesigner/latest/actions/get-indicator-info?${params}`, {
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
| `docId` | string | yes | Document ID or alias. |
| `guid` | string | yes | Indicator GUID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "acceptValueData": true,
      "description": "string",
      "guid": "string",
      "indicatorType": "string",
      "initiatives": [
        {}
      ],
      "items": [
        {}
      ],
      "measure": "string",
      "measureNames": [
        "Ava Chen"
      ],
      "name": "Ava Chen",
      "updateInterval": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `acceptValueData` | boolean | Whether the indicator accepts direct value data. |
| `description` | string | Indicator description. |
| `guid` | string | Indicator GUID. |
| `indicatorType` | string | Indicator business type. |
| `initiatives` | array<object> | Linked initiatives. |
| `items` | array<object> | Child indicator items. |
| `measure` | string | Indicator measure. |
| `measureNames` | array<string> | Localized measure names. |
| `name` | string | Indicator name. |
| `updateInterval` | string | Indicator update cadence. |

## Native endpoint

Through the native BSC Designer API, this operation is `GET /rest/api/document/:docId/kpi/:guid` (base URL `https://www.webbsc.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-indicator-info.md) for the provider-specific parameters and requirements.

