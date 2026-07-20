# Aqara Home for KR: List Gateway Subdevices

Retrieves subdevices for a gateway in Aqara Home for KR.

```
GET https://connect.mindcloud.co/v1/universal/aqaraHomeForKR/latest/actions/list-gateway-subdevices
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Aqara Home for KR `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/aqaraHomeForKR/latest/actions/list-gateway-subdevices?connectionId=$CONNECTION_ID&did=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "did": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/aqaraHomeForKR/latest/actions/list-gateway-subdevices?${params}`, {
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
| `did` | string | yes | Gateway ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "count": 1,
      "createTime": 1,
      "deviceName": "Ava Chen",
      "did": "string",
      "firmwareVersion": "string",
      "model": "string",
      "modelType": 1,
      "parentDid": "string",
      "positionId": "string",
      "state": 1,
      "success": true,
      "timeZone": "string",
      "updateTime": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `count` | number |  |
| `createTime` | number |  |
| `deviceName` | string |  |
| `did` | string |  |
| `firmwareVersion` | string |  |
| `model` | string |  |
| `modelType` | number |  |
| `parentDid` | string |  |
| `positionId` | string |  |
| `state` | number |  |
| `success` | boolean |  |
| `timeZone` | string |  |
| `updateTime` | number |  |

## Native endpoint

Through the native Aqara Home for KR API, this operation is `POST v3.0/open/api` (base URL `https://open-kr.aqara.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-gateway-subdevices.md) for the provider-specific parameters and requirements.

