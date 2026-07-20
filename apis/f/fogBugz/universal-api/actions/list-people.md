# FogBugz: List People

Retrieves people from FogBugz.

```
GET https://connect.mindcloud.co/v1/universal/fogBugz/latest/actions/list-people
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a FogBugz `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/fogBugz/latest/actions/list-people?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/fogBugz/latest/actions/list-people?${params}`, {
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
| `fIncludeActive` | boolean | no | Set to true to include active users. |
| `fIncludeNormal` | boolean | no | Set to true to include normal users. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `fIncludeDeleted` | boolean | no | Set to true to include deleted users. |
| `fIncludeCommunity` | boolean | no | Set to true to include community users. |
| `fIncludeVirtual` | boolean | no | Set to true to include virtual users. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "dtLastActivity": "string",
      "fAdministrator": true,
      "fCommunity": true,
      "fDeleted": true,
      "fNotify": true,
      "fPaletteExpanded": true,
      "fRecurseBugChildren": true,
      "fVirtual": true,
      "ixBugWorkingOn": 1,
      "ixPerson": 1,
      "sEmail": "ava@example.com",
      "sFrom": "string",
      "sFullName": "Ava Chen",
      "sHomepage": "string",
      "sLanguage": "string",
      "sLDAPUid": "string",
      "sLocale": "string",
      "sPhone": "string",
      "sTimeZoneKey": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `dtLastActivity` | string | Last activity timestamp. |
| `fAdministrator` | boolean | Whether the user is an administrator. |
| `fCommunity` | boolean | Whether the user is a community user. |
| `fDeleted` | boolean | Whether the user is deleted. |
| `fNotify` | boolean | Whether notifications are enabled. |
| `fPaletteExpanded` | boolean | Whether the palette is expanded. |
| `fRecurseBugChildren` | boolean | Whether child cases recurse. |
| `fVirtual` | boolean | Whether the user is a virtual user. |
| `ixBugWorkingOn` | number | Current working case ID. |
| `ixPerson` | number | User ID. |
| `sEmail` | string | Email address. |
| `sFrom` | string | From address. |
| `sFullName` | string | Full name. |
| `sHomepage` | string | Homepage URL. |
| `sLanguage` | string | Language key. |
| `sLDAPUid` | string | LDAP UID. |
| `sLocale` | string | Locale key. |
| `sPhone` | string | Phone number. |
| `sTimeZoneKey` | string | Time zone key. |

## Native endpoint

Through the native FogBugz API, this operation is `POST /listPeople` (base URL `{{credentials.siteUrl}}/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-people.md) for the provider-specific parameters and requirements.

