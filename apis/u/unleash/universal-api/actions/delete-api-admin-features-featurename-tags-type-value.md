# Unleash: Removes A Tag From A Feature.

Removes a tag from a feature from Unleash.

```
DELETE https://connect.mindcloud.co/v1/universal/unleash/latest/actions/delete-api-admin-features-featurename-tags-type-value
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Unleash `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/unleash/latest/actions/delete-api-admin-features-featurename-tags-type-value?connectionId=$CONNECTION_ID&featureName=Ava%20Chen&type=string&value=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "featureName": "Ava Chen",
  "type": "string",
  "value": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/unleash/latest/actions/delete-api-admin-features-featurename-tags-type-value?${params}`, {
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
| `featureName` | string | yes | Required path parameter. |
| `type` | string | yes | Required path parameter. |
| `value` | string | yes | Required path parameter. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "2026-05-07T12:00:00.000Z",
      "description": "string",
      "id": "string",
      "message": "string",
      "name": "Ava Chen",
      "success": true,
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | date | Creation timestamp. |
| `description` | string | Resource description. |
| `id` | string | Resource identifier. |
| `message` | string | Response message. |
| `name` | string | Resource name. |
| `success` | boolean | Whether the operation succeeded. |
| `updatedAt` | date | Last update timestamp. |

## Native endpoint

Through the native Unleash API, this operation is `DELETE /api/admin/features/{featureName}/tags/{type}/{value}` (base URL `https://us.app.getunleash.io/uspp0456`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-api-admin-features-featurename-tags-type-value.md) for the provider-specific parameters and requirements.

