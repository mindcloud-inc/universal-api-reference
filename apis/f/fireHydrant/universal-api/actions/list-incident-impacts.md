# FireHydrant: List Incident Impacts

Retrieves incident impacts by type from FireHydrant.

```
GET https://connect.mindcloud.co/v1/universal/fireHydrant/latest/actions/list-incident-impacts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a FireHydrant `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/fireHydrant/latest/actions/list-incident-impacts?connectionId=$CONNECTION_ID&impactType=0&incidentId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "impactType": "0",
  "incidentId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/fireHydrant/latest/actions/list-incident-impacts?${params}`, {
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
| `impactType` | list | yes | The impacted infrastructure type to list. One of: `0`, `1`, `2`, `3`. |
| `incidentId` | string | yes | The FireHydrant incident ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": [
        {
          "id": "string",
          "infrastructure": {},
          "type": "string"
        }
      ],
      "pagination": {
        "count": 1,
        "items": 1,
        "last": 1,
        "page": 1,
        "pages": 1
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data[].id` | string |  |
| `data[].infrastructure` | object |  |
| `data[].type` | string |  |
| `pagination.count` | number |  |
| `pagination.items` | number |  |
| `pagination.last` | number |  |
| `pagination.page` | number |  |
| `pagination.pages` | number |  |

## Native endpoint

Through the native FireHydrant API, this operation is `GET /incidents/:incident_id/impact/:type` (base URL `https://api.firehydrant.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-incident-impacts.md) for the provider-specific parameters and requirements.

