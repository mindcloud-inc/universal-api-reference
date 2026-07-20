# Sertifier: List Skills

Finds skills in Sertifier by search filters.

```
GET https://connect.mindcloud.co/v1/universal/sertifier/latest/actions/list-skills
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Sertifier `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sertifier/latest/actions/list-skills?connectionId=$CONNECTION_ID&limit=25&offset=0&language=en" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "language": "en"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sertifier/latest/actions/list-skills?${params}`, {
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
| `searchTerm` | string | no | Filter skills by matching title text. |
| `language` | string | yes | Skill language code. Sertifier supports en or tr. Default: `en`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "content": {},
      "data": {},
      "hasError": true,
      "isUpgraded": true,
      "message": "string",
      "showPurchaseSheet": true,
      "upgradePlan": {},
      "validationErrors": [
        {
          "key": "string",
          "value": "string"
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
| `content` | object |  |
| `data` | object |  |
| `hasError` | boolean |  |
| `isUpgraded` | boolean |  |
| `message` | string |  |
| `showPurchaseSheet` | boolean |  |
| `upgradePlan` | object |  |
| `validationErrors[].key` | string |  |
| `validationErrors[].value` | string |  |

## Native endpoint

Through the native Sertifier API, this operation is `POST /detail/searchSkills` (base URL `https://b2b.sertifier.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-skills.md) for the provider-specific parameters and requirements.

