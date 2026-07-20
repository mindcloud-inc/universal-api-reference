# EventSquare: List Zapier Trigger Examples

Retrieves Zapier trigger examples from EventSquare.

```
GET https://connect.mindcloud.co/v1/universal/eventSquare/latest/actions/list-zapier-trigger-examples
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a EventSquare `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/eventSquare/latest/actions/list-zapier-trigger-examples?connectionId=$CONNECTION_ID&type=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "type": "0"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/eventSquare/latest/actions/list-zapier-trigger-examples?${params}`, {
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
| `type` | string | yes | The EventSquare trigger type to retrieve example webhook payloads for. One of: `0`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "order": {},
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `order` | object | An example EventSquare order payload for the selected trigger. |
| `type` | string | The webhook trigger type. |

## Native endpoint

Through the native EventSquare API, this operation is `GET /1.0/integrations/zapier/triggers` (base URL `https://api.eventsquare.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-zapier-trigger-examples.md) for the provider-specific parameters and requirements.

