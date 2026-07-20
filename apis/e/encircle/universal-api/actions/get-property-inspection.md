# Encircle: Get Property Inspection

Retrieves a property inspection from Encircle by ID.

```
GET https://connect.mindcloud.co/v1/universal/encircle/latest/actions/get-property-inspection
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Encircle `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/encircle/latest/actions/get-property-inspection?connectionId=$CONNECTION_ID&propertyInspectionId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "propertyInspectionId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/encircle/latest/actions/get-property-inspection?${params}`, {
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
| `propertyInspectionId` | number | yes |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Encircle API returns.

## Native endpoint

Through the native Encircle API, this operation is `GET /v1/property_inspections/:property_inspection_id` (base URL `https://api.encircleapp.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-property-inspection.md) for the provider-specific parameters and requirements.

