# PageVitals: Update Multistep Test



```
PUT https://connect.mindcloud.co/v1/universal/pageVitals/latest/actions/update-multistep-test
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PageVitals `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/pageVitals/latest/actions/update-multistep-test" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "websiteId": "string",
  "testId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/pageVitals/latest/actions/update-multistep-test', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "websiteId": "string",
    "testId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `websiteId` | string | yes |  |
| `testId` | string | yes |  |
| `alias` | string | no |  |
| `device` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "alias": "string",
      "created": "string",
      "device": "string",
      "id": "string",
      "steps": [
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
| `alias` | string |  |
| `created` | string |  |
| `device` | string |  |
| `id` | string |  |
| `steps` | array<object> |  |

## Native endpoint

Through the native PageVitals API, this operation is `PUT /:websiteId/multistep/:testId` (base URL `https://api.pagevitals.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-multistep-test.md) for the provider-specific parameters and requirements.

