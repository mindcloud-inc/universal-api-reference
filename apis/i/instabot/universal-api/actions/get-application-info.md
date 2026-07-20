# Instabot: Get Application Info

Retrieves application details from Instabot.

```
GET https://connect.mindcloud.co/v1/universal/instabot/latest/actions/get-application-info
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Instabot `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/instabot/latest/actions/get-application-info?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/instabot/latest/actions/get-application-info?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "agencyId": 1,
      "applicationName": "Ava Chen",
      "devCompanyId": 1,
      "hideBrandedFooterInChat": true,
      "version": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `agencyId` | number |  |
| `applicationName` | string |  |
| `devCompanyId` | number |  |
| `hideBrandedFooterInChat` | boolean |  |
| `version` | string |  |

## Native endpoint

Through the native Instabot API, this operation is `GET /` (base URL `https://api.instabot.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-application-info.md) for the provider-specific parameters and requirements.

