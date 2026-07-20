# OfficeMaps: Remove Department Manager

Removes a manager from a department in OfficeMaps.

```
PUT https://connect.mindcloud.co/v1/universal/officeMaps/latest/actions/remove-department-manager
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a OfficeMaps `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/officeMaps/latest/actions/remove-department-manager" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "departmentId": "string",
  "personId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/officeMaps/latest/actions/remove-department-manager', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "departmentId": "string",
    "personId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `departmentId` | string | yes | Department UUID. |
| `personId` | string | yes | Person UUID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "failure": true,
      "notFound": true,
      "success": true,
      "unauthorized": true,
      "value": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `failure` | boolean | Whether the request failed. |
| `notFound` | boolean | Whether the target record was not found. |
| `success` | boolean | Whether the request succeeded. |
| `unauthorized` | boolean | Whether the request was unauthorized. |
| `value` | array<object> | Per-person operation results. |

## Native endpoint

Through the native OfficeMaps API, this operation is `DELETE /v1/department/:departmentId/manager/:personId` (base URL `https://api.officemaps.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/remove-department-manager.md) for the provider-specific parameters and requirements.

