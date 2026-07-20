# ManyReach: List Tag Prospects

Retrieves prospects for a tag from ManyReach.

```
GET https://connect.mindcloud.co/v1/universal/manyReach/latest/actions/list-tag-prospects
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ManyReach `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/manyReach/latest/actions/list-tag-prospects?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/manyReach/latest/actions/list-tag-prospects?${params}`, {
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
| `id` | string | no | Tag ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "baseListId": 1,
      "city": {},
      "company": {},
      "companySize": {},
      "companySocial": {},
      "country": {},
      "createdAt": "string",
      "custom1": {},
      "custom10": {},
      "custom11": {},
      "custom12": {},
      "custom13": {},
      "custom14": {},
      "custom15": {},
      "custom16": {},
      "custom17": {},
      "custom18": {},
      "custom19": {},
      "custom2": {},
      "custom20": {},
      "custom3": {},
      "custom4": {},
      "custom5": {},
      "custom6": {},
      "custom7": {},
      "custom8": {},
      "custom9": {},
      "customImageUrl": {},
      "domain": {},
      "email": "ava@example.com",
      "firstName": "Ava",
      "icebreaker": {},
      "industry": {},
      "jobPosition": {},
      "lastName": "Chen",
      "location": {},
      "logoUrl": {},
      "notes": {},
      "personalSocial": {},
      "phone": {},
      "prospectId": 1,
      "screenshotUrl": {},
      "sendingActive": true,
      "sendingStatus": "string",
      "state": {},
      "website": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `baseListId` | number |  |
| `city` | object |  |
| `company` | object |  |
| `companySize` | object |  |
| `companySocial` | object |  |
| `country` | object |  |
| `createdAt` | string |  |
| `custom1` | object |  |
| `custom10` | object |  |
| `custom11` | object |  |
| `custom12` | object |  |
| `custom13` | object |  |
| `custom14` | object |  |
| `custom15` | object |  |
| `custom16` | object |  |
| `custom17` | object |  |
| `custom18` | object |  |
| `custom19` | object |  |
| `custom2` | object |  |
| `custom20` | object |  |
| `custom3` | object |  |
| `custom4` | object |  |
| `custom5` | object |  |
| `custom6` | object |  |
| `custom7` | object |  |
| `custom8` | object |  |
| `custom9` | object |  |
| `customImageUrl` | object |  |
| `domain` | object |  |
| `email` | string |  |
| `firstName` | string |  |
| `icebreaker` | object |  |
| `industry` | object |  |
| `jobPosition` | object |  |
| `lastName` | string |  |
| `location` | object |  |
| `logoUrl` | object |  |
| `notes` | object |  |
| `personalSocial` | object |  |
| `phone` | object |  |
| `prospectId` | number |  |
| `screenshotUrl` | object |  |
| `sendingActive` | boolean |  |
| `sendingStatus` | string |  |
| `state` | object |  |
| `website` | object |  |

## Native endpoint

Through the native ManyReach API, this operation is `GET https://api.manyreach.com/api/v2/tags/:id/prospects` (base URL `https://api.manyreach.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-tag-prospects.md) for the provider-specific parameters and requirements.

