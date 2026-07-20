# Kameleoon: Get all targeting rules



```
GET https://connect.mindcloud.co/v1/universal/kameleoon/latest/actions/get-all-targeting-rules
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Kameleoon `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/kameleoon/latest/actions/get-all-targeting-rules?connectionId=$CONNECTION_ID&paramsIo=page%3D1%2C%20perPage%3D20" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "paramsIo": "page=1, perPage=20"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/kameleoon/latest/actions/get-all-targeting-rules?${params}`, {
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
| `paramsIo` | string | yes | Required query object documented by Kameleoon for list endpoints. Example: `page=1, perPage=20`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "code": "string",
      "id": 1,
      "segmentConfiguration": "string",
      "segmentId": 1,
      "siteId": 1,
      "targetingConfigurationParam": "string",
      "triggerConfiguration": "string",
      "triggerId": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `code` | string |  |
| `id` | number |  |
| `segmentConfiguration` | string |  |
| `segmentId` | number |  |
| `siteId` | number |  |
| `targetingConfigurationParam` | string |  |
| `triggerConfiguration` | string |  |
| `triggerId` | number |  |

## Native endpoint

Through the native Kameleoon API, this operation is `GET targeting-rules` (base URL `https://api.kameleoon.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-all-targeting-rules.md) for the provider-specific parameters and requirements.

