# EMnify: Get Endpoint Usage And Cost Statistics

Retrieves endpoint usage and cost statistics from EMnify.

```
GET https://connect.mindcloud.co/v1/universal/eMnify/latest/actions/get-endpoint-usage-and-cost-statistics
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a EMnify `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/eMnify/latest/actions/get-endpoint-usage-and-cost-statistics?connectionId=$CONNECTION_ID&authToken=string&endpointId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "authToken": "string",
  "endpointId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/eMnify/latest/actions/get-endpoint-usage-and-cost-statistics?${params}`, {
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
| `authToken` | string | yes | Auth token from Retrieve Authentication Token. |
| `endpointId` | number | yes | Endpoint ID to inspect. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "lastHour": {
        "data": {
          "rx": [
            {}
          ],
          "tx": [
            {}
          ]
        },
        "sms": {
          "rx": [
            {}
          ],
          "tx": [
            {}
          ]
        }
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `lastHour.data.rx[]` | object |  |
| `lastHour.data.tx[]` | object |  |
| `lastHour.sms.rx[]` | object |  |
| `lastHour.sms.tx[]` | object |  |

## Native endpoint

Through the native EMnify API, this operation is `GET /endpoint/:endpoint_id/stats` (base URL `https://cdn.emnify.net/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-endpoint-usage-and-cost-statistics.md) for the provider-specific parameters and requirements.

