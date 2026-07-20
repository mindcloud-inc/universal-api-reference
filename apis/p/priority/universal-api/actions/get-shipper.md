# Priority: Get Shipper

Retrieves a shipper from Priority.

```
GET https://connect.mindcloud.co/v1/universal/priority/latest/actions/get-shipper
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Priority `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/priority/latest/actions/get-shipper?connectionId=$CONNECTION_ID&shipperName=Ava%20Chen" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "shipperName": "Ava Chen"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/priority/latest/actions/get-shipper?${params}`, {
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
| `shipperName` | string | yes | Priority shipper key. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "CODE": "string",
      "PHONE": "string",
      "SHIPPERDES": "string",
      "SHIPPERNAME": "Ava Chen",
      "SUPNAME": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `CODE` | string |  |
| `PHONE` | string |  |
| `SHIPPERDES` | string |  |
| `SHIPPERNAME` | string |  |
| `SUPNAME` | string |  |

## Native endpoint

Through the native Priority API, this operation is `GET /SHIPPERS(SHIPPERNAME=':shipperName')` (base URL `https://t.eu.priority-connect.online/odata/Priority/tabbtd38.ini/usdemo`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-shipper.md) for the provider-specific parameters and requirements.

