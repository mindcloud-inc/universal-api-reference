# Scoro: View Event Resource

Retrieves event resource details from Scoro.

```
GET https://connect.mindcloud.co/v1/universal/scoro/latest/actions/view-event-resource
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Scoro `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/scoro/latest/actions/view-event-resource?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/scoro/latest/actions/view-event-resource?${params}`, {
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
| `id` | string | no | Scoro event resource ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "modified_date": "string",
      "resource_color": "string",
      "resource_id": 1,
      "resource_name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `modified_date` | string |  |
| `resource_color` | string |  |
| `resource_id` | number |  |
| `resource_name` | string |  |

## Native endpoint

Through the native Scoro API, this operation is `POST eventsResources/view/:id` (base URL `{{credentials.subdomain}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/view-event-resource.md) for the provider-specific parameters and requirements.

