# condoo: Delete Visitor

Deletes an existing visitor from condoo.

```
DELETE https://connect.mindcloud.co/v1/universal/condoo/latest/actions/delete-visitor
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a condoo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/condoo/latest/actions/delete-visitor?connectionId=$CONNECTION_ID&visitorId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "visitorId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/condoo/latest/actions/delete-visitor?${params}`, {
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
| `visitorId` | string | yes | Required visitor ID or visitor UUID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | number |  |

## Native endpoint

Through the native condoo API, this operation is `DELETE /visitors/{visitor_id}` (base URL `https://trk.condoo.systems/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-visitor.md) for the provider-specific parameters and requirements.

