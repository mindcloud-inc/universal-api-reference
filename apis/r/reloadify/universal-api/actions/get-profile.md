# Reloadify: Get Profile

Retrieves a profile from Reloadify.

```
GET https://connect.mindcloud.co/v1/universal/reloadify/latest/actions/get-profile
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Reloadify `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/reloadify/latest/actions/get-profile?connectionId=$CONNECTION_ID&language_id=string&profile_id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "language_id": "string",
  "profile_id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/reloadify/latest/actions/get-profile?${params}`, {
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
| `language_id` | string | yes | Language ID from the Reloadify language resource. |
| `profile_id` | string | yes | Profile ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "active": true,
      "birthdate": "string",
      "city": "string",
      "company_name": "Ava Chen",
      "country_code": "string",
      "custom_attributes": [
        {}
      ],
      "double_opt_in": true,
      "email": "ava@example.com",
      "first_name": "Ava",
      "gender": "string",
      "housenumber": "string",
      "id": "string",
      "is_company": true,
      "is_registered": true,
      "last_name": "Chen",
      "middle_name": "Ava Chen",
      "province": "string",
      "street": "string",
      "subscribed_to_newsletter": true,
      "subscribed_to_newsletter_at": "string",
      "tags": [
        "string"
      ],
      "telephone": "string",
      "unsubscribed": true,
      "zipcode": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `active` | boolean |  |
| `birthdate` | string |  |
| `city` | string |  |
| `company_name` | string |  |
| `country_code` | string |  |
| `custom_attributes` | array<object> |  |
| `double_opt_in` | boolean |  |
| `email` | string |  |
| `first_name` | string |  |
| `gender` | string |  |
| `housenumber` | string |  |
| `id` | string |  |
| `is_company` | boolean |  |
| `is_registered` | boolean |  |
| `last_name` | string |  |
| `middle_name` | string |  |
| `province` | string |  |
| `street` | string |  |
| `subscribed_to_newsletter` | boolean |  |
| `subscribed_to_newsletter_at` | string |  |
| `tags` | array<string> |  |
| `telephone` | string |  |
| `unsubscribed` | boolean |  |
| `zipcode` | string |  |

## Native endpoint

Through the native Reloadify API, this operation is `GET /v2/languages/:language_id/profiles/:profile_id` (base URL `https://api.reloadify.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-profile.md) for the provider-specific parameters and requirements.

