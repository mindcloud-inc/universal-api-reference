# Veterans Affairs Facilities: List Facility IDs

Retrieves VA facility IDs by facility type.

```
GET https://connect.mindcloud.co/v1/universal/veteransAffairsFacilities/latest/actions/list-facility-ids
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Veterans Affairs Facilities `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/veteransAffairsFacilities/latest/actions/list-facility-ids?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/veteransAffairsFacilities/latest/actions/list-facility-ids?${params}`, {
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
| `type` | list | no | Optional facility type filter. One of: `benefits`, `cemetery`, `health`, `vet_center`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string | VA facility ID. |

## Native endpoint

Through the native Veterans Affairs Facilities API, this operation is `GET /ids` (base URL `https://sandbox-api.va.gov/services/va_facilities/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-facility-ids.md) for the provider-specific parameters and requirements.

