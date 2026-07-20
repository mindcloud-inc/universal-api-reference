# Instasent: Search Audience by Phone



```
GET https://connect.mindcloud.co/v1/universal/instasent/latest/actions/search-audience-by-phone
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Instasent `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/instasent/latest/actions/search-audience-by-phone?connectionId=$CONNECTION_ID&project=string&userPhone=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "project": "string",
  "userPhone": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/instasent/latest/actions/search-audience-by-phone?${params}`, {
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
| `project` | string | yes | Instasent project uid. Use the uid value from List Projects, not the internal project id. |
| `userPhone` | string | yes | Phone number to search. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "entities": [
        {
          "attributesData": {
            "_accepts_marketing_email": {},
            "_accepts_marketing_sms": {},
            "_accepts_marketing_whatsapp": {},
            "_client_lists": {},
            "_client_tags": "string",
            "_date_imported": "string",
            "_date_registered": "string",
            "_date_seen": "string",
            "_date_updated": "string",
            "_email": "ava@example.com",
            "_first_name": "Ava",
            "_full_name": "Ava Chen",
            "_is_subscribed_email": true,
            "_is_subscribed_sms": true,
            "_is_subscribed_whatsapp": true,
            "_last_name": "Chen",
            "_phone_mobile": "string",
            "_user_id": "string"
          },
          "audienceIds": [
            "string"
          ],
          "createdAt": "string",
          "deletedAt": {},
          "dsContactIds": [
            "string"
          ],
          "dsIds": [
            "string"
          ],
          "id": "string",
          "indexedAt": "string",
          "updatedAt": "string"
        }
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `entities[].attributesData._accepts_marketing_email` | object |  |
| `entities[].attributesData._accepts_marketing_sms` | object |  |
| `entities[].attributesData._accepts_marketing_whatsapp` | object |  |
| `entities[].attributesData._client_lists` | object |  |
| `entities[].attributesData._client_tags` | string |  |
| `entities[].attributesData._date_imported` | string |  |
| `entities[].attributesData._date_registered` | string |  |
| `entities[].attributesData._date_seen` | string |  |
| `entities[].attributesData._date_updated` | string |  |
| `entities[].attributesData._email` | string |  |
| `entities[].attributesData._first_name` | string |  |
| `entities[].attributesData._full_name` | string |  |
| `entities[].attributesData._is_subscribed_email` | boolean |  |
| `entities[].attributesData._is_subscribed_sms` | boolean |  |
| `entities[].attributesData._is_subscribed_whatsapp` | boolean |  |
| `entities[].attributesData._last_name` | string |  |
| `entities[].attributesData._phone_mobile` | string |  |
| `entities[].attributesData._user_id` | string |  |
| `entities[].audienceIds[]` | string |  |
| `entities[].createdAt` | string |  |
| `entities[].deletedAt` | object |  |
| `entities[].dsContactIds[]` | string |  |
| `entities[].dsIds[]` | string |  |
| `entities[].id` | string |  |
| `entities[].indexedAt` | string |  |
| `entities[].updatedAt` | string |  |

## Native endpoint

Through the native Instasent API, this operation is `GET /project/:project/audience/search/phone/:userPhone` (base URL `https://api.instasent.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-audience-by-phone.md) for the provider-specific parameters and requirements.

