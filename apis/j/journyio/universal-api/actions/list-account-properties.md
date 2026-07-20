# Journy.io: List Account Properties



```
GET https://connect.mindcloud.co/v1/universal/journyio/latest/actions/list-account-properties
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Journy.io `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/journyio/latest/actions/list-account-properties?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/journyio/latest/actions/list-account-properties?${params}`, {
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
      "group": {
        "id": "string",
        "name": "Ava Chen"
      },
      "isComputed": true,
      "label": "string",
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `group.id` | string | Property group identifier. |
| `group.name` | string | Property group name. |
| `isComputed` | boolean | Whether the property is computed by Journy.io. |
| `label` | string | Human-readable property label. |
| `name` | string | Property key. |

## Native endpoint

Through the native Journy.io API, this operation is `GET /properties/accounts` (base URL `https://api.journy.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-account-properties.md) for the provider-specific parameters and requirements.

