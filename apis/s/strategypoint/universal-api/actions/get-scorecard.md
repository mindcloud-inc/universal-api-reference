# Strategypoint: Get Scorecard

Retrieves a scorecard from Strategypoint.

```
GET https://connect.mindcloud.co/v1/universal/strategypoint/latest/actions/get-scorecard
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Strategypoint `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/strategypoint/latest/actions/get-scorecard?connectionId=$CONNECTION_ID&scorecardId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "scorecardId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/strategypoint/latest/actions/get-scorecard?${params}`, {
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
| `scorecardId` | number | yes | The unique ClearPoint scorecard identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "active": true,
      "archived": true,
      "favorite": true,
      "mission": "string",
      "name": "Ava Chen",
      "ownerId": 1,
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
| `mission` | string | The scorecard mission statement. |
| `name` | string | The scorecard name. |
| `ownerId` | number | The owning user identifier. |
| `scorecardId` | number | The unique scorecard identifier. |
| `vision` | string | The scorecard vision statement. |

## Native endpoint

Through the native Strategypoint API, this operation is `GET /scorecards/{scorecardId}` (base URL `https://app.clearpointstrategy.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-scorecard.md) for the provider-specific parameters and requirements.

