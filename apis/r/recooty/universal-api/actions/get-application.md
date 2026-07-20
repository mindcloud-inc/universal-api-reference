# Recooty: Get Application



```
GET https://connect.mindcloud.co/v1/universal/recooty/latest/actions/get-application
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Recooty `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/recooty/latest/actions/get-application?connectionId=$CONNECTION_ID&applicationId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "applicationId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/recooty/latest/actions/get-application?${params}`, {
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
| `applicationId` | string | yes | The Recooty application ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "application": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `application` | object | The requested application record. |

## Native endpoint

Through the native Recooty API, this operation is `GET /v1/applications/{{applicationId}}` (base URL `https://standaloneapi.recooty.app/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-application.md) for the provider-specific parameters and requirements.

