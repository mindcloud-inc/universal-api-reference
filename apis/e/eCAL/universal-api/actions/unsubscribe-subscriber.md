# ECAL: Unsubscribe Subscriber

Unsubscribes a subscriber from ECAL.

```
DELETE https://connect.mindcloud.co/v1/universal/eCAL/latest/actions/unsubscribe-subscriber
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ECAL `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/eCAL/latest/actions/unsubscribe-subscriber?connectionId=$CONNECTION_ID&ecalId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "ecalId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/eCAL/latest/actions/unsubscribe-subscriber?${params}`, {
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
| `ecalId` | string | yes | Subscriber ecal_id value. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "ecalId": "string",
      "message": "string",
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `ecalId` | string |  |
| `message` | string |  |
| `success` | boolean |  |

## Native endpoint

Through the native ECAL API, this operation is `POST /subscriber/:ecalId/unsubscribe` (base URL `https://api.ecal.com/apiv2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/unsubscribe-subscriber.md) for the provider-specific parameters and requirements.

