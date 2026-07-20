# Zoho FSM: List Work Order Transitions

Retrieves available work order transitions from Zoho FSM.

```
GET https://connect.mindcloud.co/v1/universal/zohoFSM/latest/actions/list-work-order-transitions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoho FSM `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zohoFSM/latest/actions/list-work-order-transitions?connectionId=$CONNECTION_ID&recordId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "recordId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zohoFSM/latest/actions/list-work-order-transitions?${params}`, {
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
| `recordId` | string | yes | The Zoho FSM record ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "code": "string",
      "processInfo": {
        "apiName": "Ava Chen",
        "fieldId": "string",
        "fieldLabel": "string",
        "fieldValue": "string",
        "name": "Ava Chen"
      },
      "status": "string",
      "transitions": [
        {
          "actionType": "string",
          "enabled": true,
          "fields": [
            {
              "dataType": "string",
              "displayLabel": "string",
              "id": "string",
              "mandatory": true,
              "transitionSequence": 1
            }
          ],
          "id": "string",
          "name": "Ava Chen",
          "nextFieldValue": "string",
          "type": "string"
        }
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `code` | string |  |
| `processInfo.apiName` | string |  |
| `processInfo.fieldId` | string |  |
| `processInfo.fieldLabel` | string |  |
| `processInfo.fieldValue` | string |  |
| `processInfo.name` | string |  |
| `status` | string |  |
| `transitions[].actionType` | string |  |
| `transitions[].enabled` | boolean |  |
| `transitions[].fields[].dataType` | string |  |
| `transitions[].fields[].displayLabel` | string |  |
| `transitions[].fields[].id` | string |  |
| `transitions[].fields[].mandatory` | boolean |  |
| `transitions[].fields[].transitionSequence` | number |  |
| `transitions[].id` | string |  |
| `transitions[].name` | string |  |
| `transitions[].nextFieldValue` | string |  |
| `transitions[].type` | string |  |

## Native endpoint

Through the native Zoho FSM API, this operation is `GET /Work_Orders/:recordId/actions/blueprint/transitions` (base URL `{{credentials.accessTokenRequest.api_domain}}/fsm/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-work-order-transitions.md) for the provider-specific parameters and requirements.

