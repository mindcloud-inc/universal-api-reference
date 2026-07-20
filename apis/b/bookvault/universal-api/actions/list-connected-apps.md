# Bookvault: List Connected Apps

Retrieves connected apps from your Bookvault account.

```
GET https://connect.mindcloud.co/v1/universal/bookvault/latest/actions/list-connected-apps
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Bookvault `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bookvault/latest/actions/list-connected-apps?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/bookvault/latest/actions/list-connected-apps?${params}`, {
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
      "AppID": 1,
      "Authorised": true,
      "Name": "Ava Chen",
      "Partner": true,
      "Settings": {},
      "Type": "string",
      "URL": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `AppID` | number |  |
| `Authorised` | boolean |  |
| `Name` | string |  |
| `Partner` | boolean |  |
| `Settings` | object |  |
| `Type` | string |  |
| `URL` | string |  |

## Native endpoint

Through the native Bookvault API, this operation is `GET /App` (base URL `https://api.bookvault.app/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-connected-apps.md) for the provider-specific parameters and requirements.

