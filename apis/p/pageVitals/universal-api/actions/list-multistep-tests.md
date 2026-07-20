# PageVitals: List Multistep Tests



```
GET https://connect.mindcloud.co/v1/universal/pageVitals/latest/actions/list-multistep-tests
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PageVitals `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pageVitals/latest/actions/list-multistep-tests?connectionId=$CONNECTION_ID&websiteId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "websiteId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pageVitals/latest/actions/list-multistep-tests?${params}`, {
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
| `websiteId` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "alias": "string",
      "cls": 1,
      "created": "string",
      "device": "string",
      "duration": 1,
      "id": "string",
      "inp": 1,
      "state": "string",
      "steps": [
        {}
      ],
      "successRate": 1,
      "successRates": [
        {}
      ],
      "tbt": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `alias` | string |  |
| `cls` | number |  |
| `created` | string |  |
| `device` | string |  |
| `duration` | number |  |
| `id` | string |  |
| `inp` | number |  |
| `state` | string |  |
| `steps` | array<object> |  |
| `successRate` | number |  |
| `successRates` | array<object> |  |
| `tbt` | number |  |

## Native endpoint

Through the native PageVitals API, this operation is `GET /:websiteId/multistep` (base URL `https://api.pagevitals.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-multistep-tests.md) for the provider-specific parameters and requirements.

