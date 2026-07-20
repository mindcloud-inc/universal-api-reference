# Port API AI: Update Scorecard

Updates a scorecard in Port.

```
PUT https://connect.mindcloud.co/v1/universal/portAPIAI/latest/actions/update-scorecard
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Port API AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/portAPIAI/latest/actions/update-scorecard" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "blueprintIdentifier": "string",
  "identifier": "string",
  "rules[]": [
    {}
  ],
  "scorecardIdentifier": "string",
  "title": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/portAPIAI/latest/actions/update-scorecard', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "blueprintIdentifier": "string",
    "identifier": "string",
    "rules[]": [{}],
    "scorecardIdentifier": "string",
    "title": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `blueprintIdentifier` | string | yes | The Port blueprint identifier. |
| `identifier` | string | yes | Scorecard identifier |
| `rules[]` | array<object> | yes | Scorecard rules |
| `scorecardIdentifier` | string | yes | The Port scorecard identifier. |
| `title` | string | yes | Scorecard title |

## Response

```json
{
  "success": true,
  "data": [
    {
      "ok": true,
      "scorecard": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `ok` | boolean |  |
| `scorecard` | object |  |

## Native endpoint

Through the native Port API AI API, this operation is `PUT /blueprints/:blueprint_identifier/scorecards/:scorecard_identifier` (base URL `https://api.port.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-scorecard.md) for the provider-specific parameters and requirements.

