# Aqara Home for KR: Get Position Details

Retrieves position details from Aqara Home for KR.

```
GET https://connect.mindcloud.co/v1/universal/aqaraHomeForKR/latest/actions/get-position-details
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Aqara Home for KR `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/aqaraHomeForKR/latest/actions/get-position-details?connectionId=$CONNECTION_ID&positionIds%5B%5D=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "positionIds[]": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/aqaraHomeForKR/latest/actions/get-position-details?${params}`, {
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
| `positionIds[]` | array<string> | yes | Position ID array. Maximum 50 values. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createTime": 1,
      "description": "string",
      "parentPositionId": "string",
      "positionId": "string",
      "positionName": "Ava Chen",
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createTime` | number |  |
| `description` | string |  |
| `parentPositionId` | string |  |
| `positionId` | string |  |
| `positionName` | string |  |
| `success` | boolean |  |

## Native endpoint

Through the native Aqara Home for KR API, this operation is `POST v3.0/open/api` (base URL `https://open-kr.aqara.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-position-details.md) for the provider-specific parameters and requirements.

