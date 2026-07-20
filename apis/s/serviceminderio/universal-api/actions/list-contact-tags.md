# serviceminder.io: List Contact Tags

Retrieves tags for a contact from ServiceMinder.

```
GET https://connect.mindcloud.co/v1/universal/serviceminderio/latest/actions/list-contact-tags
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a serviceminder.io `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/serviceminderio/latest/actions/list-contact-tags?connectionId=$CONNECTION_ID&contactId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "contactId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/serviceminderio/latest/actions/list-contact-tags?${params}`, {
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
| `contactId` | number | yes | Contact identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "message": "string",
      "resultCode": 1,
      "tagList": [
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
| `message` | string |  |
| `resultCode` | number |  |
| `tagList` | array<object> |  |

## Native endpoint

Through the native serviceminder.io API, this operation is `POST /contacts/listtags` (base URL `https://serviceminder.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-contact-tags.md) for the provider-specific parameters and requirements.

