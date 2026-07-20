# Control D: Get Default Rule

Retrieves the default rule from Control D.

```
GET https://connect.mindcloud.co/v1/universal/controlD/latest/actions/get-default-rule
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Control D `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/controlD/latest/actions/get-default-rule?connectionId=$CONNECTION_ID&profileId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "profileId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/controlD/latest/actions/get-default-rule?${params}`, {
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
| `profileId` | string | yes | Primary key (PK) of the profile |

## Response

```json
{
  "success": true,
  "data": [
    {
      "do": 1,
      "status": 1,
      "via": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `do` | number |  |
| `status` | number |  |
| `via` | string |  |

## Native endpoint

Through the native Control D API, this operation is `GET /profiles/:profileId/default` (base URL `https://api.controld.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-default-rule.md) for the provider-specific parameters and requirements.

