# Aqara Home for KR: Delete Position

Deletes an existing position from Aqara Home for KR.

```
DELETE https://connect.mindcloud.co/v1/universal/aqaraHomeForKR/latest/actions/delete-position
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Aqara Home for KR `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/aqaraHomeForKR/latest/actions/delete-position?connectionId=$CONNECTION_ID&positionId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "positionId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/aqaraHomeForKR/latest/actions/delete-position?${params}`, {
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
| `positionId` | string | yes | Position ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `success` | boolean |  |

## Native endpoint

Through the native Aqara Home for KR API, this operation is `POST v3.0/open/api` (base URL `https://open-kr.aqara.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-position.md) for the provider-specific parameters and requirements.

