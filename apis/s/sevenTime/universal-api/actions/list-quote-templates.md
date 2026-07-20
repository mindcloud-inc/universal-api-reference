# Seven Time: List Quote Templates

Retrieves quote templates from Seven Time.

```
GET https://connect.mindcloud.co/v1/universal/sevenTime/latest/actions/list-quote-templates
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Seven Time `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sevenTime/latest/actions/list-quote-templates?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sevenTime/latest/actions/list-quote-templates?${params}`, {
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
      "columnContents": [
        "string"
      ],
      "createDate": "2026-05-07T12:00:00.000Z",
      "createdByUser": "string",
      "createdByUserName": "Ava Chen",
      "documents": [
        {}
      ],
      "footerNumOfCols": 1,
      "footerText": "string",
      "Id": "string",
      "language": "string",
      "logo": [
        {}
      ],
      "logoPosition": "string",
      "logotypeWidth": 1,
      "overrideFooter": true,
      "overrideLogoAndAddress": true,
      "quoteAddress": "string",
      "quoteElements": [
        {}
      ],
      "quoteType": 1,
      "templateName": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `columnContents` | array<string> |  |
| `createDate` | date |  |
| `createdByUser` | string |  |
| `createdByUserName` | string |  |
| `documents` | array<object> |  |
| `footerNumOfCols` | number |  |
| `footerText` | string |  |
| `Id` | string |  |
| `language` | string |  |
| `logo` | array<object> |  |
| `logoPosition` | string |  |
| `logotypeWidth` | number |  |
| `overrideFooter` | boolean |  |
| `overrideLogoAndAddress` | boolean |  |
| `quoteAddress` | string |  |
| `quoteElements` | array<object> |  |
| `quoteType` | number |  |
| `templateName` | string |  |

## Native endpoint

Through the native Seven Time API, this operation is `GET /quoteTemplates` (base URL `https://app.seventime.se/api/2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-quote-templates.md) for the provider-specific parameters and requirements.

