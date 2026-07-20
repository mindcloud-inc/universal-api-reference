# ManyReach: List Campaign Sequences

Retrieves sequences for a campaign from ManyReach.

```
GET https://connect.mindcloud.co/v1/universal/manyReach/latest/actions/list-campaign-sequences
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ManyReach `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/manyReach/latest/actions/list-campaign-sequences?connectionId=$CONNECTION_ID&id=123" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "123"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/manyReach/latest/actions/list-campaign-sequences?${params}`, {
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
| `id` | number | yes | Campaign ID for fetching sequences. Example: `123`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "conditionAction": "string",
      "conditionExtra": true,
      "conditionNegate": true,
      "conditionOperator": "string",
      "conditionReply": "string",
      "conditionTimes": 1,
      "name": "Ava Chen",
      "sequenceId": 1,
      "shortName": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `conditionAction` | string |  |
| `conditionExtra` | boolean |  |
| `conditionNegate` | boolean |  |
| `conditionOperator` | string |  |
| `conditionReply` | string |  |
| `conditionTimes` | number |  |
| `name` | string |  |
| `sequenceId` | number |  |
| `shortName` | string |  |

## Native endpoint

Through the native ManyReach API, this operation is `GET https://api.manyreach.com/api/v2/campaigns/:id/sequences` (base URL `https://api.manyreach.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-campaign-sequences.md) for the provider-specific parameters and requirements.

