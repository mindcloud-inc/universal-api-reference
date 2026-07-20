# Recruitee ATS: List Offers



```
GET https://connect.mindcloud.co/v1/universal/recruiteeATS/latest/actions/list-offers
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Recruitee ATS `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/recruiteeATS/latest/actions/list-offers?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/recruiteeATS/latest/actions/list-offers?${params}`, {
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
      "careersJobPageLayoutId": {},
      "category": "string",
      "closedAt": {},
      "createdAt": "string",
      "departmentId": {},
      "education": "string",
      "employmentType": "string",
      "example": true,
      "experience": "string",
      "followed": true,
      "guid": "string",
      "hiringManagerId": {},
      "id": 1,
      "langCode": "string",
      "mailboxEmail": "ava@example.com",
      "pipelineTemplateId": 1,
      "position": 1,
      "priority": {},
      "publishedAt": {},
      "recruiterId": {},
      "slug": "string",
      "status": "string",
      "title": "string",
      "updatedAt": "string",
      "wysiwygEditor": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `careersJobPageLayoutId` | object |  |
| `category` | string |  |
| `closedAt` | object |  |
| `createdAt` | string |  |
| `departmentId` | object |  |
| `education` | string |  |
| `employmentType` | string |  |
| `example` | boolean |  |
| `experience` | string |  |
| `followed` | boolean |  |
| `guid` | string |  |
| `hiringManagerId` | object |  |
| `id` | number |  |
| `langCode` | string |  |
| `mailboxEmail` | string |  |
| `pipelineTemplateId` | number |  |
| `position` | number |  |
| `priority` | object |  |
| `publishedAt` | object |  |
| `recruiterId` | object |  |
| `slug` | string |  |
| `status` | string |  |
| `title` | string |  |
| `updatedAt` | string |  |
| `wysiwygEditor` | string |  |

## Native endpoint

Through the native Recruitee ATS API, this operation is `GET /c/:company_id/offers` (base URL `https://api.recruitee.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-offers.md) for the provider-specific parameters and requirements.

