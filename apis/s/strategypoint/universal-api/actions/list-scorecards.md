# Strategypoint: List Scorecards

Retrieves scorecards from Strategypoint.

```
GET https://connect.mindcloud.co/v1/universal/strategypoint/latest/actions/list-scorecards
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Strategypoint `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/strategypoint/latest/actions/list-scorecards?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/strategypoint/latest/actions/list-scorecards?${params}`, {
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
| `page` | number | no | Page number. |
| `count` | number | no | Count per page. |
| `include` | string | no | Include deleted or menu data. |
| `userId` | number | no | Limit the results to one user. |
| `periodId` | number | no | Reporting period ID. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `fields` | string | no | Comma-separated list of fields to return. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "active": true,
      "archived": true,
      "favorite": true,
      "name": "Ava Chen",
      "ownerId": 1,
      "periodId": 1,
      "scorecardId": 1,
      "vision": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `active` | boolean | Whether the scorecard is active. |
| `archived` | boolean | Whether the scorecard is archived. |
| `favorite` | boolean | Whether the scorecard is marked as a favorite. |
| `name` | string | The scorecard name. |
| `ownerId` | number | The owning user identifier. |
| `periodId` | number | The current period identifier. |
| `scorecardId` | number | The unique scorecard identifier. |
| `vision` | string | The scorecard vision statement. |

## Native endpoint

Through the native Strategypoint API, this operation is `GET /scorecards` (base URL `https://app.clearpointstrategy.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-scorecards.md) for the provider-specific parameters and requirements.

