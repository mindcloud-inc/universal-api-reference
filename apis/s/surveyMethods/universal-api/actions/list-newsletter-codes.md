# SurveyMethods: List Newsletter Codes



```
GET https://connect.mindcloud.co/v1/universal/surveyMethods/latest/actions/list-newsletter-codes
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SurveyMethods `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/surveyMethods/latest/actions/list-newsletter-codes?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/surveyMethods/latest/actions/list-newsletter-codes?${params}`, {
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
      "pages": [
        {
          "newsletters": [
            {
              "code": "string",
              "title": "string"
            }
          ],
          "number": 1
        }
      ],
      "rowcount": 1,
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `pages` | array<object> |  |
| `pages[].newsletters` | array<object> |  |
| `pages[].newsletters[].code` | string |  |
| `pages[].newsletters[].title` | string |  |
| `pages[].number` | number |  |
| `rowcount` | number |  |
| `status` | string |  |

## Native endpoint

Through the native SurveyMethods API, this operation is `GET /:loginId/:apiKey/newsletters/codes/` (base URL `https://api.surveymethods.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-newsletter-codes.md) for the provider-specific parameters and requirements.

