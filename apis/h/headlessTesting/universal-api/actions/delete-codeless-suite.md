# Headless Testing: Delete Codeless Suite

Deletes a codeless suite from Headless Testing.

```
DELETE https://connect.mindcloud.co/v1/universal/headlessTesting/latest/actions/delete-codeless-suite
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Headless Testing `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/headlessTesting/latest/actions/delete-codeless-suite?connectionId=$CONNECTION_ID&suiteId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "suiteId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/headlessTesting/latest/actions/delete-codeless-suite?${params}`, {
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
| `suiteId` | string | yes | The codeless suite identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": 1,
      "message": "string",
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | number |  |
| `message` | string |  |
| `success` | boolean |  |

## Native endpoint

Through the native Headless Testing API, this operation is `DELETE /labsuites/:suiteId` (base URL `https://api.testingbot.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-codeless-suite.md) for the provider-specific parameters and requirements.

