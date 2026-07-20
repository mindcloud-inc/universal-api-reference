# EMnify: List SIM Statuses

Retrieves available SIM statuses from EMnify.

```
GET https://connect.mindcloud.co/v1/universal/eMnify/latest/actions/list-sim-statuses
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a EMnify `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/eMnify/latest/actions/list-sim-statuses?connectionId=$CONNECTION_ID&authToken=Paste%20the%20auth_token%20from%20Retrieve%20Authentication%20Token" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "authToken": "Paste the auth_token from Retrieve Authentication Token"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/eMnify/latest/actions/list-sim-statuses?${params}`, {
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
| `authToken` | string | yes | Auth token from Retrieve Authentication Token. Example: `Paste the auth_token from Retrieve Authentication Token`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "description": "string",
      "id": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `description` | string |  |
| `id` | number |  |

## Native endpoint

Through the native EMnify API, this operation is `GET /sim/status` (base URL `https://cdn.emnify.net/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-sim-statuses.md) for the provider-specific parameters and requirements.

