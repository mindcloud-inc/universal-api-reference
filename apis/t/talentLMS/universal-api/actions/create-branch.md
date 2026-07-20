# TalentLMS: Create Branch

Creates a new branch in TalentLMS.

```
POST https://connect.mindcloud.co/v1/universal/talentLMS/latest/actions/create-branch
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a TalentLMS `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/talentLMS/latest/actions/create-branch" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen",
  "description": "string",
  "defaultLocale": "ar-AE"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/talentLMS/latest/actions/create-branch', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Ava Chen",
    "description": "string",
    "defaultLocale": "ar-AE"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | yes | Branch name. |
| `description` | string | yes | Branch description. |
| `defaultLocale` | list | yes | Branch default locale code. One of: `ar-AE`, `az-AZ`, `bs-BA`, `ca-ES`, `cs-CZ`, `da-DK`, `de-DE`, `el-GR`, `en-US`, `es-ES`, `et-EE`, `fa-IR`, `fi-FI`, `fr-FR`, `he-IL`, `hi-IN`, `hr-HR`, `hu-HU`, `hy-AM`, `id-ID`, `is-IS`, `it-IT`, `ja-JP`, `ka-GE`, `ko-KR`, `lt-LT`, `lv-LV`, `mn-MN`, `ms-MY`, `nb-NO`, `nl-NL`, `pl-PL`, `pt-BR`, `pt-PT`, `ro-RO`, `ru-RU`, `sk-SK`, `sl-SI`, `sr-RS`, `sv-SE`, `th-TH`, `tr-TR`, `uk-UA`, `vi-VN`, `zh-CN`, `zh-TW`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "active": true,
      "defaultGroup": {},
      "defaultLocale": "string",
      "defaultTimezone": "string",
      "defaultUserType": {},
      "description": "string",
      "ecommerce": {},
      "id": 1,
      "name": "Ava Chen",
      "ownerId": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `active` | boolean |  |
| `defaultGroup` | object |  |
| `defaultLocale` | string |  |
| `defaultTimezone` | string |  |
| `defaultUserType` | object |  |
| `description` | string |  |
| `ecommerce` | object |  |
| `id` | number |  |
| `name` | string |  |
| `ownerId` | number |  |

## Native endpoint

Through the native TalentLMS API, this operation is `POST /branches` (base URL `https://{{credentials.domain}}.talentlms.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-branch.md) for the provider-specific parameters and requirements.

