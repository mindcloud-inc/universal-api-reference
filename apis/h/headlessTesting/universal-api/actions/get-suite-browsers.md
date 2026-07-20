# Headless Testing: Get Suite Browsers

Retrieves browser assignments for a codeless suite from Headless Testing.

```
GET https://connect.mindcloud.co/v1/universal/headlessTesting/latest/actions/get-suite-browsers
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Headless Testing `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/headlessTesting/latest/actions/get-suite-browsers?connectionId=$CONNECTION_ID&suiteId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "suiteId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/headlessTesting/latest/actions/get-suite-browsers?${params}`, {
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
      "items": [
        {}
      ],
      "total": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `items` | array<object> |  |
| `total` | number |  |

## Native endpoint

Through the native Headless Testing API, this operation is `GET /labsuites/:suiteId/browsers` (base URL `https://api.testingbot.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-suite-browsers.md) for the provider-specific parameters and requirements.

