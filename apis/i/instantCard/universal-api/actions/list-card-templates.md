# InstantCard: List Card Templates

Retrieves available card templates from InstantCard.

```
GET https://connect.mindcloud.co/v1/universal/instantCard/latest/actions/list-card-templates
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a InstantCard `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/instantCard/latest/actions/list-card-templates?connectionId=$CONNECTION_ID&organizationId=20003827" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "organizationId": "20003827"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/instantCard/latest/actions/list-card-templates?${params}`, {
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
| `organizationId` | number | yes | Organization ID from InstantCard. Example: `20003827`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": 1,
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | number | Card template ID. |
| `name` | string | Card template name. |

## Native endpoint

Through the native InstantCard API, this operation is `GET /api/v2/organizations/:organizationId/card_templates` (base URL `https://core.instantcard.net`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-card-templates.md) for the provider-specific parameters and requirements.

