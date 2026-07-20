# TOPdesk: Get Incident Progress Trail Count

Retrieves an incident progress trail count from TOPdesk.

```
GET https://connect.mindcloud.co/v1/universal/tOPdesk/latest/actions/get-incident-progress-trail-count
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a TOPdesk `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/tOPdesk/latest/actions/get-incident-progress-trail-count?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/tOPdesk/latest/actions/get-incident-progress-trail-count?${params}`, {
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
| `id` | string | yes | Incident identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "count": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `count` | number |  |

## Native endpoint

Through the native TOPdesk API, this operation is `GET /incidents/id/:id/progresstrail/count` (base URL `https://usatopdesktrial2.topdesk.net/tas/api/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-incident-progress-trail-count.md) for the provider-specific parameters and requirements.

