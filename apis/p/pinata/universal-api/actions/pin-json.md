# Pinata: Pin JSON

Creates a new pinned JSON object in Pinata.

```
POST https://connect.mindcloud.co/v1/universal/pinata/latest/actions/pin-json
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Pinata `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/pinata/latest/actions/pin-json" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "pinataContent": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/pinata/latest/actions/pin-json', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "pinataContent": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `pinataContent` | object | yes | JSON object to pin to IPFS. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "GroupId": "string",
      "ID": "string",
      "IpfsHash": "string",
      "Keyvalues": {},
      "MimeType": "string",
      "Name": "Ava Chen",
      "NumberOfFiles": 1,
      "PinSize": 1,
      "Timestamp": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `GroupId` | string |  |
| `ID` | string |  |
| `IpfsHash` | string |  |
| `Keyvalues` | object |  |
| `MimeType` | string |  |
| `Name` | string |  |
| `NumberOfFiles` | number |  |
| `PinSize` | number |  |
| `Timestamp` | date |  |

## Native endpoint

Through the native Pinata API, this operation is `POST /pinning/pinJSONToIPFS` (base URL `https://api.pinata.cloud`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/pin-json.md) for the provider-specific parameters and requirements.

