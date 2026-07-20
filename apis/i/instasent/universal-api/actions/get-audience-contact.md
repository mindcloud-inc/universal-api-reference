# Instasent: Get Audience Contact



```
GET https://connect.mindcloud.co/v1/universal/instasent/latest/actions/get-audience-contact
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Instasent `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/instasent/latest/actions/get-audience-contact?connectionId=$CONNECTION_ID&project=string&audienceId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "project": "string",
  "audienceId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/instasent/latest/actions/get-audience-contact?${params}`, {
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
| `audienceId` | string | yes | Audience identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "entity": {
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
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `entity.attributesData._accepts_marketing_email` | object |  |
| `entity.attributesData._accepts_marketing_sms` | object |  |
| `entity.attributesData._accepts_marketing_whatsapp` | object |  |
| `entity.attributesData._client_lists` | object |  |
| `entity.attributesData._client_tags` | string |  |
| `entity.attributesData._date_imported` | string |  |
| `entity.attributesData._date_registered` | string |  |
| `entity.attributesData._date_seen` | string |  |
| `entity.attributesData._date_updated` | string |  |
| `entity.attributesData._email` | string |  |
| `entity.attributesData._first_name` | string |  |
| `entity.attributesData._full_name` | string |  |
| `entity.attributesData._is_subscribed_email` | boolean |  |
| `entity.attributesData._is_subscribed_sms` | boolean |  |
| `entity.attributesData._is_subscribed_whatsapp` | boolean |  |
| `entity.attributesData._last_name` | string |  |
| `entity.attributesData._phone_mobile` | string |  |
| `entity.attributesData._user_id` | string |  |
| `entity.audienceIds[]` | string |  |
| `entity.createdAt` | string |  |
| `entity.deletedAt` | object |  |
| `entity.dsContactIds[]` | string |  |
| `entity.dsIds[]` | string |  |
| `entity.id` | string |  |
| `entity.indexedAt` | string |  |
| `entity.updatedAt` | string |  |

## Native endpoint

Through the native Instasent API, this operation is `GET /project/:project/audience/:audienceId` (base URL `https://api.instasent.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-audience-contact.md) for the provider-specific parameters and requirements.

