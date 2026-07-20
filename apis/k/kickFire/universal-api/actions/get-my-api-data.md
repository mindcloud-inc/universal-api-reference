# KickFire: Get My API Data

Retrieves MyAPI custom account attributes from KickFire.

```
GET https://connect.mindcloud.co/v1/universal/kickFire/latest/actions/get-my-api-data
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a KickFire `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/kickFire/latest/actions/get-my-api-data?connectionId=$CONNECTION_ID&keyField=twitter.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "keyField": "twitter.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/kickFire/latest/actions/get-my-api-data?${params}`, {
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
| `keyField` | string | yes | Lookup value accepted by the MyAPI endpoint. Example: `twitter.com`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "results": 1,
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `results` | number |  |
| `status` | string |  |

## Native endpoint

Through the native KickFire API, this operation is `GET /my` (base URL `https://api.kickfire.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-my-api-data.md) for the provider-specific parameters and requirements.

