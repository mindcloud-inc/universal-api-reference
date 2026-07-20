# Stormboard: Get Storm Access

Retrieves your access level for a Storm in Stormboard.

```
GET https://connect.mindcloud.co/v1/universal/stormboard/latest/actions/get-storm-access
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Stormboard `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/stormboard/latest/actions/get-storm-access?connectionId=$CONNECTION_ID&stormId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "stormId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/stormboard/latest/actions/get-storm-access?${params}`, {
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
| `stormId` | number | yes | Storm ID from the Stormboard share dialog or related storm record. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "administrator": true,
      "status": 1,
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `administrator` | boolean |  |
| `status` | number |  |
| `type` | string |  |

## Native endpoint

Through the native Stormboard API, this operation is `GET /storms/:storm_id/access` (base URL `https://api.stormboard.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-storm-access.md) for the provider-specific parameters and requirements.

