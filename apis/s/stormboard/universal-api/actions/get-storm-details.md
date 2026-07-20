# Stormboard: Get Storm Details

Retrieves Storm details from Stormboard.

```
GET https://connect.mindcloud.co/v1/universal/stormboard/latest/actions/get-storm-details
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Stormboard `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/stormboard/latest/actions/get-storm-details?connectionId=$CONNECTION_ID&stormId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "stormId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/stormboard/latest/actions/get-storm-details?${params}`, {
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
| `thumbnail` | string | no | Optional storm thumbnail value. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "status": 1,
      "storm": {
        "admin": 1,
        "goals": "string",
        "ideastyle": "string",
        "key": "string",
        "legendpalette": "string",
        "readonly": 1,
        "status": "string",
        "title": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `status` | number |  |
| `storm` | object |  |
| `storm.admin` | number |  |
| `storm.goals` | string |  |
| `storm.ideastyle` | string |  |
| `storm.key` | string |  |
| `storm.legendpalette` | string |  |
| `storm.readonly` | number |  |
| `storm.status` | string |  |
| `storm.title` | string |  |

## Native endpoint

Through the native Stormboard API, this operation is `GET /storms/:storm_id` (base URL `https://api.stormboard.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-storm-details.md) for the provider-specific parameters and requirements.

