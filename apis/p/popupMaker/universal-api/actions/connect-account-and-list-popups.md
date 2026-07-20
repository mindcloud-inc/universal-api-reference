# Popup Maker: Connect Account and List Popups

Retrieves connected account details and popups from Popup Maker.

```
GET https://connect.mindcloud.co/v1/universal/popupMaker/latest/actions/connect-account-and-list-popups
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Popup Maker `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/popupMaker/latest/actions/connect-account-and-list-popups?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/popupMaker/latest/actions/connect-account-and-list-popups?${params}`, {
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
      "isAuthenticate": true,
      "popups": {},
      "user": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `isAuthenticate` | boolean | Whether the Popup Maker API key authenticated successfully. |
| `popups` | object | Popup inventory returned by Popup Maker for the connected account. |
| `user` | object | Connected Popup Maker account details. |

## Native endpoint

Through the native Popup Maker API, this operation is `POST app/connect` (base URL `https://popupmaker.com/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/connect-account-and-list-popups.md) for the provider-specific parameters and requirements.

