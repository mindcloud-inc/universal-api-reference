# Strategypoint: Get Measure

Retrieves a measure from Strategypoint.

```
GET https://connect.mindcloud.co/v1/universal/strategypoint/latest/actions/get-measure
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Strategypoint `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/strategypoint/latest/actions/get-measure?connectionId=$CONNECTION_ID&measureId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "measureId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/strategypoint/latest/actions/get-measure?${params}`, {
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
| `measureId` | number | yes | The unique measure identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "completed": true,
      "description": "string",
      "favorite": true,
      "lastEdited": "string",
      "name": "Ava Chen",
      "objectId": 1,
      "ownerId": 1,
      "scorecardId": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `completed` | boolean | Whether the measure is completed. |
| `description` | string | The measure description. |
| `favorite` | boolean | Whether the measure is a favorite. |
| `lastEdited` | string | The last-edited timestamp. |
| `name` | string | The measure name. |
| `objectId` | number | The measure identifier. |
| `ownerId` | number | The owning user identifier. |
| `scorecardId` | number | The related scorecard identifier. |

## Native endpoint

Through the native Strategypoint API, this operation is `GET /measures/{measureId}` (base URL `https://app.clearpointstrategy.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-measure.md) for the provider-specific parameters and requirements.

