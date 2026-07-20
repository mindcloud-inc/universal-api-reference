# OfficeMaps: Bulk Add Department Administrators

Adds multiple administrators to a department in OfficeMaps.

```
PUT https://connect.mindcloud.co/v1/universal/officeMaps/latest/actions/bulk-add-department-administrators
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a OfficeMaps `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/officeMaps/latest/actions/bulk-add-department-administrators" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "departmentId": "string",
  "operations[]": [
    {}
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/officeMaps/latest/actions/bulk-add-department-administrators', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "departmentId": "string",
    "operations[]": [{}]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `departmentId` | string | yes | Department UUID. |
| `operations[]` | array<object> | yes | People to apply in the bulk request. |

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

Through the native OfficeMaps API, this operation is `PUT /v1/department/:departmentId/administrators` (base URL `https://api.officemaps.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/bulk-add-department-administrators.md) for the provider-specific parameters and requirements.

