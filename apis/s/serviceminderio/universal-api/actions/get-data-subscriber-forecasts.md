# serviceminder.io: Get Data Subscriber Forecasts

Retrieves data subscriber forecasts from ServiceMinder.

```
GET https://connect.mindcloud.co/v1/universal/serviceminderio/latest/actions/get-data-subscriber-forecasts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a serviceminder.io `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/serviceminderio/latest/actions/get-data-subscriber-forecasts?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/serviceminderio/latest/actions/get-data-subscriber-forecasts?${params}`, {
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
| `fromDate` | date | no | Forecast start date. |
| `throughDate` | date | no | Forecast end date. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "message": "string",
      "organizations": [
        {}
      ],
      "resultCode": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `message` | string |  |
| `organizations` | array<object> |  |
| `resultCode` | number |  |

## Native endpoint

Through the native serviceminder.io API, this operation is `POST /datasubscriber/forecasts` (base URL `https://serviceminder.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-data-subscriber-forecasts.md) for the provider-specific parameters and requirements.

