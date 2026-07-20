# Aqara Home for KR: List Devices

Retrieves devices from Aqara Home for KR.

```
GET https://connect.mindcloud.co/v1/universal/aqaraHomeForKR/latest/actions/list-devices
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Aqara Home for KR `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/aqaraHomeForKR/latest/actions/list-devices?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/aqaraHomeForKR/latest/actions/list-devices?${params}`, {
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
| `dids[]` | array<string> | no | Device ID array. Up to 100 device IDs can be queried at a time. |
| `positionId` | string | no | Position ID. Leave empty to query all devices under the user. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `pageNum` | number | no | Page number. Default is 1. Default: `1`. |
| `pageSize` | number | no | Number of items per page. Default is 50. Default: `50`. |

## Response

```json
{
  "success": true,
  "data": [
    {
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
      "totalCount": 1,
      "updateTime": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
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
| `totalCount` | number |  |
| `updateTime` | number |  |

## Native endpoint

Through the native Aqara Home for KR API, this operation is `POST v3.0/open/api` (base URL `https://open-kr.aqara.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-devices.md) for the provider-specific parameters and requirements.

