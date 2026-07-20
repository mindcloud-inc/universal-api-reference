# HIPAAtizer: Count Future Appointments

Retrieves the count of future appointments in HIPAAtizer.

```
GET https://connect.mindcloud.co/v1/universal/hIPAAtizer/latest/actions/count-future-appointments
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a HIPAAtizer `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/hIPAAtizer/latest/actions/count-future-appointments?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/hIPAAtizer/latest/actions/count-future-appointments?${params}`, {
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

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `request` | object | no | Optional raw request wrapper. Use `{}` when running without filters. |
| `request.locationIds` | list<string> | no | Optional location UUID filters. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "count": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `count` | number |  |

## Native endpoint

Through the native HIPAAtizer API, this operation is `POST /api/v1/api_key/appointments/count_future` (base URL `https://app.hipaatizer.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/count-future-appointments.md) for the provider-specific parameters and requirements.

