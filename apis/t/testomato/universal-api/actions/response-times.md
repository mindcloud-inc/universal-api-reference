# Testomato: Response times

Retrieves project response times from Testomato.

```
GET https://connect.mindcloud.co/v1/universal/testomato/latest/actions/response-times
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Testomato `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/testomato/latest/actions/response-times?connectionId=$CONNECTION_ID&id=string&start=2026-05-07T12%3A00%3A00.000Z" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string",
  "start": "2026-05-07T12:00:00.000Z"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/testomato/latest/actions/response-times?${params}`, {
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
| `id` | string | yes |  |
| `start` | date | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "contentDownloadTime": 1,
      "dnsLookupTime": 1,
      "initialConnectionTime": 1,
      "requestTime": 1,
      "responseDate": "string",
      "sslTime": 1,
      "totalResponseTime": 1,
      "waitingTime": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `contentDownloadTime` | number |  |
| `dnsLookupTime` | number |  |
| `initialConnectionTime` | number |  |
| `requestTime` | number |  |
| `responseDate` | string |  |
| `sslTime` | number |  |
| `totalResponseTime` | number |  |
| `waitingTime` | number |  |

## Native endpoint

Through the native Testomato API, this operation is `GET /project/:id/responseTimes` (base URL `https://testomato.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/response-times.md) for the provider-specific parameters and requirements.

