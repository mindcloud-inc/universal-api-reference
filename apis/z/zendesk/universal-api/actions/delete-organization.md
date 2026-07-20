# Zendesk: Delete Organization

Deletes an existing organization from Zendesk.

```
DELETE https://connect.mindcloud.co/v1/universal/zendesk/latest/actions/delete-organization
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zendesk `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/zendesk/latest/actions/delete-organization?connectionId=$CONNECTION_ID&id=46843791853460" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "46843791853460"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zendesk/latest/actions/delete-organization?${params}`, {
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
| `id` | number | yes | Organization ID Example: `46843791853460`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "value": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `value` | object | Empty response body returned when the organization is deleted successfully. |

## Native endpoint

Through the native Zendesk API, this operation is `DELETE /organizations/:id.json` (base URL `https://{{credentials.subdomain}}.zendesk.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-organization.md) for the provider-specific parameters and requirements.

