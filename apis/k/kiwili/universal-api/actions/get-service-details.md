# Kiwili: Get Service Details

Retrieves details for a service in Kiwili.

```
GET https://connect.mindcloud.co/v1/universal/kiwili/latest/actions/get-service-details
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Kiwili `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/kiwili/latest/actions/get-service-details?connectionId=$CONNECTION_ID&service_id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "service_id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/kiwili/latest/actions/get-service-details?${params}`, {
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
| `service_id` | number | yes | The Kiwili service ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "Active": true,
      "Billable": true,
      "Id": 1,
      "Name": "Ava Chen",
      "Rate": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `Active` | boolean |  |
| `Billable` | boolean |  |
| `Id` | number |  |
| `Name` | string |  |
| `Rate` | number |  |

## Native endpoint

Through the native Kiwili API, this operation is `GET /service/:service_id` (base URL `https://mindcloud.kiwili.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-service-details.md) for the provider-specific parameters and requirements.

