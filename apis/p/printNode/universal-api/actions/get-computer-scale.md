# PrintNode: Get Computer Scale

Retrieves a specific scale from PrintNode.

```
GET https://connect.mindcloud.co/v1/universal/printNode/latest/actions/get-computer-scale
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PrintNode `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/printNode/latest/actions/get-computer-scale?connectionId=$CONNECTION_ID&computerId=string&deviceName=Ava%20Chen&deviceNumber=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "computerId": "string",
  "deviceName": "Ava Chen",
  "deviceNumber": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/printNode/latest/actions/get-computer-scale?${params}`, {
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
| `computerId` | string | yes | PrintNode computer ID. |
| `deviceName` | string | yes | Scale device name from PrintNode. |
| `deviceNumber` | string | yes | Scale device number from PrintNode. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "ageOfData": 1,
      "clientReportedCreateTimestamp": "2026-05-07T12:00:00.000Z",
      "computerId": 1,
      "deviceName": "Ava Chen",
      "deviceNum": 1,
      "mass": [
        1
      ],
      "measurement": {
        "g": 1
      },
      "port": "string",
      "product": "string",
      "productId": 1,
      "vendor": "string",
      "vendorId": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `ageOfData` | number | Age of the latest reading in milliseconds. |
| `clientReportedCreateTimestamp` | date | Timestamp when the client reported the reading. |
| `computerId` | number | Computer identifier. |
| `deviceName` | string | Scale device name. |
| `deviceNum` | number | Scale device number on the computer. |
| `mass` | array<number> | Scale mass values reported by PrintNode. |
| `measurement.g` | number | Latest scale measurement in grams. |
| `port` | string | Port or device path reported by PrintNode. |
| `product` | string | Scale product name. |
| `productId` | number | Scale product identifier. |
| `vendor` | string | Scale vendor name. |
| `vendorId` | number | Scale vendor identifier. |

## Native endpoint

Through the native PrintNode API, this operation is `GET /computer/:computerId/scale/:deviceName/:deviceNumber` (base URL `https://api.printnode.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-computer-scale.md) for the provider-specific parameters and requirements.

