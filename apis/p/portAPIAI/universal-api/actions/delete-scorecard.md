# Port API AI: Delete Scorecard

Deletes a scorecard from Port.

```
DELETE https://connect.mindcloud.co/v1/universal/portAPIAI/latest/actions/delete-scorecard
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Port API AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/portAPIAI/latest/actions/delete-scorecard?connectionId=$CONNECTION_ID&blueprintIdentifier=string&scorecardIdentifier=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "blueprintIdentifier": "string",
  "scorecardIdentifier": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/portAPIAI/latest/actions/delete-scorecard?${params}`, {
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
| `blueprintIdentifier` | string | yes | The Port blueprint identifier. |
| `scorecardIdentifier` | string | yes | The Port scorecard identifier. |

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

Through the native Port API AI API, this operation is `DELETE /blueprints/:blueprint_identifier/scorecards/:scorecard_identifier` (base URL `https://api.port.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-scorecard.md) for the provider-specific parameters and requirements.

