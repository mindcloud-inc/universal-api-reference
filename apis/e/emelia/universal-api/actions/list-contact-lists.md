# Emelia: List Contact Lists

Retrieves contact lists from Emelia.

```
GET https://connect.mindcloud.co/v1/universal/emelia/latest/actions/list-contact-lists
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Emelia `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/emelia/latest/actions/list-contact-lists?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/emelia/latest/actions/list-contact-lists?${params}`, {
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
      "data": {
        "contactLists": [
          {
            "contactCount": 1,
            "fields": [
              "string"
            ],
            "name": "Ava Chen",
            "usedInCampaign": true
          }
        ]
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data.contactLists[].contactCount` | number |  |
| `data.contactLists[].fields[]` | string |  |
| `data.contactLists[].name` | string |  |
| `data.contactLists[].usedInCampaign` | boolean |  |

## Native endpoint

Through the native Emelia API, this operation is `POST /graphql` (base URL `https://graphql.emelia.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-contact-lists.md) for the provider-specific parameters and requirements.

