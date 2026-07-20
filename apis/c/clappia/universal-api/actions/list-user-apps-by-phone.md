# Clappia: List User Apps by Phone

Retrieves user apps from Clappia by phone number.

```
GET https://connect.mindcloud.co/v1/universal/clappia/latest/actions/list-user-apps-by-phone
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Clappia `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/clappia/latest/actions/list-user-apps-by-phone?connectionId=$CONNECTION_ID&phoneNumber=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "phoneNumber": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/clappia/latest/actions/list-user-apps-by-phone?${params}`, {
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
| `phoneNumber` | string | yes | Phone number of the workplace user whose apps should be returned. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "appId": "string",
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `appId` | string | Clappia app ID. |
| `name` | string | Clappia app name. |

## Native endpoint

Through the native Clappia API, this operation is `GET /workplace/getUserApps` (base URL `https://api-public-v4.clappia.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-user-apps-by-phone.md) for the provider-specific parameters and requirements.

