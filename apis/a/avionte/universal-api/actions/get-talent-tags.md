# Avionte: Get Talent Tags



```
GET https://connect.mindcloud.co/v1/universal/avionte/latest/actions/get-talent-tags
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Avionte `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/avionte/latest/actions/get-talent-tags?connectionId=$CONNECTION_ID&talentId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "talentId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/avionte/latest/actions/get-talent-tags?${params}`, {
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
| `talentId` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "customFields": {},
      "resumeSkills": [
        {
          "id": 1,
          "name": "Ava Chen",
          "talentId": 1,
          "value": 1
        }
      ],
      "skills": [
        {
          "descriptionId": 1,
          "positionId": 1,
          "skillDescription": "string",
          "skillId": 1,
          "skillPosition": "string",
          "talentId": 1
        }
      ],
      "sources": [
        {
          "expirationDate": {},
          "id": 1,
          "sourceId": 1,
          "sourceName": "Ava Chen",
          "talentId": 1
        }
      ],
      "tags": [
        {
          "detail": "string",
          "detailId": 1,
          "expirationDate": {},
          "tag": "string",
          "tagId": 1,
          "talentId": 1,
          "talentTagId": 1
        }
      ],
      "talentId": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `customFields` | object |  |
| `resumeSkills[].id` | number |  |
| `resumeSkills[].name` | string |  |
| `resumeSkills[].talentId` | number |  |
| `resumeSkills[].value` | number |  |
| `skills[].descriptionId` | number |  |
| `skills[].positionId` | number |  |
| `skills[].skillDescription` | string |  |
| `skills[].skillId` | number |  |
| `skills[].skillPosition` | string |  |
| `skills[].talentId` | number |  |
| `sources[].expirationDate` | object |  |
| `sources[].id` | number |  |
| `sources[].sourceId` | number |  |
| `sources[].sourceName` | string |  |
| `sources[].talentId` | number |  |
| `tags[].detail` | string |  |
| `tags[].detailId` | number |  |
| `tags[].expirationDate` | object |  |
| `tags[].tag` | string |  |
| `tags[].tagId` | number |  |
| `tags[].talentId` | number |  |
| `tags[].talentTagId` | number |  |
| `talentId` | number |  |

## Native endpoint

Through the native Avionte API, this operation is `GET /front-office/v1/talent/:talentId/all-tags` (base URL `https://api.avionte.com/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-talent-tags.md) for the provider-specific parameters and requirements.

