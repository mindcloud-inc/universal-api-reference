# MOBIDI: List Allowed Login Providers

Retrieves allowed login providers from MOBIDI.

```
GET https://connect.mindcloud.co/v1/universal/mOBIDI/latest/actions/list-allowed-login-providers
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a MOBIDI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mOBIDI/latest/actions/list-allowed-login-providers?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/mOBIDI/latest/actions/list-allowed-login-providers?${params}`, {
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
      "__WebEditorMode": 1,
      "Description": "string",
      "DisplayName": "Ava Chen",
      "IconName": "Ava Chen",
      "ID": "string",
      "IsReady": true,
      "LoginGUIInfo": {},
      "LoginPageUrl": "https://example.com",
      "TypeName": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `__WebEditorMode` | number | Provider editor mode. |
| `Description` | string | Provider description. |
| `DisplayName` | string | User-facing login provider label. |
| `IconName` | string | Optional icon identifier. |
| `ID` | string | Provider identifier. |
| `IsReady` | boolean | Whether the provider is configured and ready. |
| `LoginGUIInfo` | object | Login form behavior metadata. |
| `LoginPageUrl` | string | Login page route when the provider uses an external sign-in flow. |
| `TypeName` | string | Internal login provider type. |

## Native endpoint

Through the native MOBIDI API, this operation is `GET /UserManagementService` (base URL `https://servis2.dece.com.tr`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-allowed-login-providers.md) for the provider-specific parameters and requirements.

