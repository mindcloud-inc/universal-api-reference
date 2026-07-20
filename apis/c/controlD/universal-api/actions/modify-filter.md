# Control D: Modify Filter

Updates a filter for a profile in Control D.

```
PUT https://connect.mindcloud.co/v1/universal/controlD/latest/actions/modify-filter
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Control D `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/controlD/latest/actions/modify-filter" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "profileId": "string",
  "filter": "string",
  "status": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/controlD/latest/actions/modify-filter', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "profileId": "string",
    "filter": "string",
    "status": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `profileId` | string | yes | Primary key (PK) of the profile |
| `filter` | string | yes | Filter name |
| `status` | number | yes | Status of the filter. 1 to enable, 0 to disable. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "value": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `value` | string | Filter identifier returned by the filter update response. |

## Native endpoint

Through the native Control D API, this operation is `PUT /profiles/:profileId/filters/filter/:filter` (base URL `https://api.controld.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/modify-filter.md) for the provider-specific parameters and requirements.

