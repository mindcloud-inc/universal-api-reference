# Bookvault: List Address Groups

Retrieves address groups from your Bookvault account.

```
GET https://connect.mindcloud.co/v1/universal/bookvault/latest/actions/list-address-groups
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Bookvault `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bookvault/latest/actions/list-address-groups?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/bookvault/latest/actions/list-address-groups?${params}`, {
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
      "ContactListID": 1,
      "ContactListName": "Ava Chen",
      "DateAdded": "string",
      "DateCreated": "string",
      "Members": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `ContactListID` | number |  |
| `ContactListName` | string |  |
| `DateAdded` | string |  |
| `DateCreated` | string |  |
| `Members` | array<object> |  |

## Native endpoint

Through the native Bookvault API, this operation is `GET /AddressLists` (base URL `https://api.bookvault.app/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-address-groups.md) for the provider-specific parameters and requirements.

