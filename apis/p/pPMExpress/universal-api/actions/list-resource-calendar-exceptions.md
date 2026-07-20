# PPM Express: List Resource Calendar Exceptions



```
GET https://connect.mindcloud.co/v1/universal/pPMExpress/latest/actions/list-resource-calendar-exceptions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PPM Express `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pPMExpress/latest/actions/list-resource-calendar-exceptions?connectionId=$CONNECTION_ID&id=f13a87b7-d7b2-4ee8-a530-3b7c954502dc" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "f13a87b7-d7b2-4ee8-a530-3b7c954502dc"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pPMExpress/latest/actions/list-resource-calendar-exceptions?${params}`, {
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
| `id` | string | yes | The resource calendar ID whose exceptions to list. Default: `f13a87b7-d7b2-4ee8-a530-3b7c954502dc`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": [
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
| `data` | array<object> | The resource calendar exceptions. |

## Native endpoint

Through the native PPM Express API, this operation is `GET /@:tenantName/v1.0/resourcecalendar/:id/exceptions` (base URL `https://api-us.ppm.express`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-resource-calendar-exceptions.md) for the provider-specific parameters and requirements.

