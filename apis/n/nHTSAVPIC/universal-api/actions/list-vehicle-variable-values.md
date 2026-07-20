# NHTSA vPIC: List Vehicle Variable Values

Retrieves vehicle variable values from NHTSA vPIC.

```
GET https://connect.mindcloud.co/v1/universal/nHTSAVPIC/latest/actions/list-vehicle-variable-values
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a NHTSA vPIC `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/nHTSAVPIC/latest/actions/list-vehicle-variable-values?connectionId=$CONNECTION_ID&variable=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "variable": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/nHTSAVPIC/latest/actions/list-vehicle-variable-values?${params}`, {
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
| `variable` | string | yes | Full vehicle variable name or exact variable ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "elementName": "Ava Chen",
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
| `elementName` | string |  |
| `id` | number |  |
| `name` | string |  |

## Native endpoint

Through the native NHTSA vPIC API, this operation is `GET vehicles/GetVehicleVariableValuesList/:variable` (base URL `https://vpic.nhtsa.dot.gov/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-vehicle-variable-values.md) for the provider-specific parameters and requirements.

