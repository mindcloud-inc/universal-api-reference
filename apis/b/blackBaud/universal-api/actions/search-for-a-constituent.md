# BlackBaud: Search For A Constituent



```
GET https://connect.mindcloud.co/v1/universal/blackBaud/latest/actions/search-for-a-constituent
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a BlackBaud `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/blackBaud/latest/actions/search-for-a-constituent?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/blackBaud/latest/actions/search-for-a-constituent?${params}`, {
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
| `keyName` | string | no | Last name for individuals or organization name for organizations. Example: `Last name or organization name`. |
| `firstName` | string | no | The constituent first name. Example: `First name`. |
| `lookupId` | string | no | The constituent lookup ID. Example: `Lookup ID`. |
| `emailAddress` | string | no | The constituent email address. Example: `name@example.org`. |
| `phoneNumber` | string | no | The constituent phone number. Example: `5551234567`. |
| `includeIndividuals` | boolean | no | Include individual constituents. Example: `true`. |
| `includeOrganizations` | boolean | no | Include organization constituents. Example: `true`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `exactMatchOnly` | boolean | no | Match all criteria exactly. Example: `false`. |
| `includeDeceased` | boolean | no | Include deceased constituents. Example: `false`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native BlackBaud API returns.

## Native endpoint

Through the native BlackBaud API, this operation is `GET alt-conmg/constituents/search` (base URL `https://api.sky.blackbaud.com/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-for-a-constituent.md) for the provider-specific parameters and requirements.

