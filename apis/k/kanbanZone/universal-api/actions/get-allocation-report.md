# Kanban Zone: Get Allocation Report

Retrieves an allocation report from Kanban Zone.

```
GET https://connect.mindcloud.co/v1/universal/kanbanZone/latest/actions/get-allocation-report
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Kanban Zone `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/kanbanZone/latest/actions/get-allocation-report?connectionId=$CONNECTION_ID&board=string&groupBy=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "board": "string",
  "groupBy": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/kanbanZone/latest/actions/get-allocation-report?${params}`, {
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
| `board` | string | yes | The board public ID. |
| `groupBy` | string | yes | Group-by criteria: label, owner, column_state, or custom_field. |
| `customField` | string | no | Custom field label to use when Group By is custom_field |
| `includeCards` | boolean | no | Include card ID arrays in the response |

## Response

```json
{
  "success": true,
  "data": [
    {
      "cards": [
        "string"
      ],
      "group": "string",
      "total": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `cards` | array<string> |  |
| `group` | string |  |
| `total` | number |  |

## Native endpoint

Through the native Kanban Zone API, this operation is `GET /board/:board/reports/allocation` (base URL `https://integrations.kanbanzone.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-allocation-report.md) for the provider-specific parameters and requirements.

