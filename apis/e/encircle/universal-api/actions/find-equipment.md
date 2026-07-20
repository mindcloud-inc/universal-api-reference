# Encircle: Find Equipment

Retrieves equipment from Encircle.

```
GET https://connect.mindcloud.co/v1/universal/encircle/latest/actions/find-equipment
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Encircle `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/encircle/latest/actions/find-equipment?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/encircle/latest/actions/find-equipment?${params}`, {
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
| `organizationId` | string | no |  |
| `isRetired` | boolean | no |  |
| `equipmentType` | list | no | One of: `air_mover`, `air_scrubber`, `dehumidifier`, `dryer`, `heater`, `other`. |
| `currentlyPlacedInClaimId` | number | no |  |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `order` | list | no | One of: `newest`, `oldest`. |
| `limit` | number | no |  |
| `after` | string | no |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Encircle API returns.

## Native endpoint

Through the native Encircle API, this operation is `GET /v2/equipment` (base URL `https://api.encircleapp.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/find-equipment.md) for the provider-specific parameters and requirements.

