# Apollo: List Contact Stages

Retrieves available contact stages from Apollo.

```
GET https://connect.mindcloud.co/v1/universal/apolloio/latest/actions/list-contact-stages
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Apollo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/apolloio/latest/actions/list-contact-stages?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/apolloio/latest/actions/list-contact-stages?${params}`, {
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
      "category": "string",
      "displayName": "Ava Chen",
      "displayOrder": 1,
      "id": "string",
      "ignoreTriggerOverride": {},
      "isMeetingSet": {},
      "name": "Ava Chen",
      "teamId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `category` | string |  |
| `displayName` | string |  |
| `displayOrder` | number |  |
| `id` | string |  |
| `ignoreTriggerOverride` | object |  |
| `isMeetingSet` | object |  |
| `name` | string |  |
| `teamId` | string |  |

## Native endpoint

Through the native Apollo API, this operation is `GET v1/contact_stages` (base URL `https://app.apollo.io/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-contact-stages.md) for the provider-specific parameters and requirements.

