# Billingo: Convert Legacy ID

Retrieves a Billingo v3 ID from legacy ID.

```
GET https://connect.mindcloud.co/v1/universal/billingo/latest/actions/convert-legacy-id
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Billingo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/billingo/latest/actions/convert-legacy-id?connectionId=$CONNECTION_ID&id=317377" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "317377"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/billingo/latest/actions/convert-legacy-id?${params}`, {
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
| `id` | number | yes | Legacy Billingo ID to convert to a v3 ID. Default: `317377`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": 1,
      "legacy_id": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | number |  |
| `legacy_id` | number |  |

## Native endpoint

Through the native Billingo API, this operation is `GET /utils/convert-legacy-id/:id` (base URL `https://api.billingo.hu/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/convert-legacy-id.md) for the provider-specific parameters and requirements.

