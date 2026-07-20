# ManyReach: List Prospects

Retrieves prospects from ManyReach.

```
GET https://connect.mindcloud.co/v1/universal/manyReach/latest/actions/list-prospects
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ManyReach `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/manyReach/latest/actions/list-prospects?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/manyReach/latest/actions/list-prospects?${params}`, {
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
      "baseListId": 1,
      "city": "string",
      "company": "string",
      "companySize": "string",
      "companySocial": "string",
      "country": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "custom1": "string",
      "custom10": "string",
      "custom11": "string",
      "custom12": "string",
      "custom13": "string",
      "custom14": "string",
      "custom15": "string",
      "custom16": "string",
      "custom17": "string",
      "custom18": "string",
      "custom19": "string",
      "custom2": "string",
      "custom20": "string",
      "custom3": "string",
      "custom4": "string",
      "custom5": "string",
      "custom6": "string",
      "custom7": "string",
      "custom8": "string",
      "custom9": "string",
      "customImageUrl": "https://example.com",
      "domain": "string",
      "email": "ava@example.com",
      "firstName": "Ava",
      "icebreaker": "string",
      "industry": "string",
      "jobPosition": "string",
      "lastName": "Chen",
      "location": "string",
      "logoUrl": "https://example.com",
      "notes": "string",
      "personalSocial": "string",
      "phone": "string",
      "prospectId": 1,
      "screenshotUrl": "https://example.com",
      "sendingActive": true,
      "sendingStatus": "string",
      "state": "string",
      "website": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `baseListId` | number | Base mailing list identifier that this prospect belongs to; must be a positive integer. |
| `city` | string | City where the prospect is located; maximum 512 characters. |
| `company` | string | Company name where the prospect works; maximum 512 characters. |
| `companySize` | string | Company size description or employee count range; maximum 32 characters. |
| `companySocial` | string | Social media profile URL for the prospect's company; maximum 512 characters. |
| `country` | string | Country where the prospect is located; maximum 512 characters. |
| `createdAt` | date | Timestamp when the prospect was created in the system. |
| `custom1` | string | Custom field 1 for storing additional prospect-specific data; maximum 2,000 characters. |
| `custom10` | string | Custom field 10 for storing additional prospect-specific data; maximum 2,000 characters. |
| `custom11` | string | Custom field 11 for storing additional prospect-specific data; maximum 2,000 characters. |
| `custom12` | string | Custom field 12 for storing additional prospect-specific data; maximum 2,000 characters. |
| `custom13` | string | Custom field 13 for storing additional prospect-specific data; maximum 2,000 characters. |
| `custom14` | string | Custom field 14 for storing additional prospect-specific data; maximum 2,000 characters. |
| `custom15` | string | Custom field 15 for storing additional prospect-specific data; maximum 2,000 characters. |
| `custom16` | string | Custom field 16 for storing additional prospect-specific data; maximum 2,000 characters. |
| `custom17` | string | Custom field 17 for storing additional prospect-specific data; maximum 2,000 characters. |
| `custom18` | string | Custom field 18 for storing additional prospect-specific data; maximum 2,000 characters. |
| `custom19` | string | Custom field 19 for storing additional prospect-specific data; maximum 2,000 characters. |
| `custom2` | string | Custom field 2 for storing additional prospect-specific data; maximum 2,000 characters. |
| `custom20` | string | Custom field 20 for storing additional prospect-specific data; maximum 2,000 characters. |
| `custom3` | string | Custom field 3 for storing additional prospect-specific data; maximum 2,000 characters. |
| `custom4` | string | Custom field 4 for storing additional prospect-specific data; maximum 2,000 characters. |
| `custom5` | string | Custom field 5 for storing additional prospect-specific data; maximum 2,000 characters. |
| `custom6` | string | Custom field 6 for storing additional prospect-specific data; maximum 2,000 characters. |
| `custom7` | string | Custom field 7 for storing additional prospect-specific data; maximum 2,000 characters. |
| `custom8` | string | Custom field 8 for storing additional prospect-specific data; maximum 2,000 characters. |
| `custom9` | string | Custom field 9 for storing additional prospect-specific data; maximum 2,000 characters. |
| `customImageUrl` | string | URL to custom image associated with the prospect; maximum 256 characters. |
| `domain` | string | Company domain name extracted from email or website; maximum 180 characters. |
| `email` | string | Email address of the prospect; must be valid email format with maximum 256 characters. |
| `firstName` | string | Prospect's first name for personalization; maximum 512 characters. |
| `icebreaker` | string | Personalized icebreaker message or conversation starter for this prospect; maximum 4,000 characters. |
| `industry` | string | Industry sector or business category of the prospect's company; maximum 512 characters. |
| `jobPosition` | string | Job title or position of the prospect within their organization; maximum 512 characters. |
| `lastName` | string | Prospect's last name for personalization; maximum 512 characters. |
| `location` | string | Geographic location or address of the prospect; maximum 512 characters. |
| `logoUrl` | string | URL to company logo image; maximum 256 characters. |
| `notes` | string | General notes or comments about this prospect for internal reference. |
| `personalSocial` | string | Personal social media profile URL (LinkedIn, Twitter, etc.); maximum 512 characters. |
| `phone` | string | Contact phone number; maximum 512 characters. |
| `prospectId` | number | Unique identifier for the prospect record. |
| `screenshotUrl` | string | URL to screenshot of the prospect's website or profile; maximum 256 characters. |
| `sendingActive` | boolean | Indicates whether the prospect is active and eligible for sending in campaigns. |
| `sendingStatus` | string | Current sending status code indicating the prospect's campaign participation state. |
| `state` | string | State or province where the prospect is located; maximum 128 characters. |
| `website` | string | Company website URL; maximum 512 characters. |

## Native endpoint

Through the native ManyReach API, this operation is `GET https://api.manyreach.com/api/v2/prospects` (base URL `https://api.manyreach.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-prospects.md) for the provider-specific parameters and requirements.

