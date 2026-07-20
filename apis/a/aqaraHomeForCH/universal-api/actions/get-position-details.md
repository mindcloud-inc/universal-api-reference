# Aqara Home for CH: Get Position Details

Retrieves Aqara Home for CH position details by ID.

```
GET https://connect.mindcloud.co/v1/universal/aqaraHomeForCH/latest/actions/get-position-details
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Aqara Home for CH `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/aqaraHomeForCH/latest/actions/get-position-details?connectionId=$CONNECTION_ID&data=%5Bobject%20Object%5D" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "data": "[object Object]"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/aqaraHomeForCH/latest/actions/get-position-details?${params}`, {
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
| `data` | object | yes | Aqara request data object for the selected intent. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createTime": "string",
      "description": "string",
      "parentPositionId": "string",
      "positionId": "string",
      "positionName": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createTime` | string | Create time. |
| `description` | string | Position description. |
| `parentPositionId` | string | Parent position id. |
| `positionId` | string | Position id. |
| `positionName` | string | Position name. |

## Native endpoint

Through the native Aqara Home for CH API, this operation is `POST /v3.0/open/api` (base URL `https://open-cn.aqara.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-position-details.md) for the provider-specific parameters and requirements.

