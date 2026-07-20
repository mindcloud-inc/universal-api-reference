# Aqara Home for KR: List Positions

Retrieves subordinate positions in Aqara Home for KR.

```
GET https://connect.mindcloud.co/v1/universal/aqaraHomeForKR/latest/actions/list-positions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Aqara Home for KR `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/aqaraHomeForKR/latest/actions/list-positions?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/aqaraHomeForKR/latest/actions/list-positions?${params}`, {
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
| `parentPositionId` | string | no | Parent position ID. Leave empty to query all positions under the user or project. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `pageNum` | number | no | Page number. Default is 1. Default: `1`. |
| `pageSize` | number | no | Number of items per page. Default is 30. Default: `30`. |

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
      "success": true,
      "totalCount": 1
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
| `totalCount` | number |  |

## Native endpoint

Through the native Aqara Home for KR API, this operation is `POST v3.0/open/api` (base URL `https://open-kr.aqara.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-positions.md) for the provider-specific parameters and requirements.

