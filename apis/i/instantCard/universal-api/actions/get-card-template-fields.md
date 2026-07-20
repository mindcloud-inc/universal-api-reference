# InstantCard: Get Card Template Fields

Retrieves card template fields from InstantCard.

```
GET https://connect.mindcloud.co/v1/universal/instantCard/latest/actions/get-card-template-fields
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a InstantCard `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/instantCard/latest/actions/get-card-template-fields?connectionId=$CONNECTION_ID&organizationId=20003827&id=17280" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "organizationId": "20003827",
  "id": "17280"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/instantCard/latest/actions/get-card-template-fields?${params}`, {
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
| `id` | number | yes | Card template ID from InstantCard. Example: `17280`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "dimensions": {},
      "label": "string",
      "legacy_token": "string",
      "token": "string",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `dimensions` | object | Field dimensions when provided. |
| `label` | string | Template field label. |
| `legacy_token` | string | Legacy template field token. |
| `token` | string | Template field token. |
| `type` | string | Template field type. |

## Native endpoint

Through the native InstantCard API, this operation is `GET /api/v2/organizations/:organizationId/card_templates/:id/fields` (base URL `https://core.instantcard.net`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-card-template-fields.md) for the provider-specific parameters and requirements.

