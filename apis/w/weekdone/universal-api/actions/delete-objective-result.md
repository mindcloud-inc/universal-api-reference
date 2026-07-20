# Weekdone: Delete Objective Result

Deletes a key result from an objective in Weekdone.

```
DELETE https://connect.mindcloud.co/v1/universal/weekdone/latest/actions/delete-objective-result
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Weekdone `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/weekdone/latest/actions/delete-objective-result?connectionId=$CONNECTION_ID&objectiveId=1&resultId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "objectiveId": "1",
  "resultId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/weekdone/latest/actions/delete-objective-result?${params}`, {
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
| `objectiveId` | number | yes |  |
| `resultId` | number | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `status` | string |  |

## Native endpoint

Through the native Weekdone API, this operation is `DELETE objective/:objectiveId/result/:resultId` (base URL `https://api.weekdone.com/1/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-objective-result.md) for the provider-specific parameters and requirements.

